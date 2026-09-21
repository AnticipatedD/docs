# Assets

This directory contains the logic for serving, processing, and validating static assets used in the GitHub Docs application. While the actual asset files (images, CSVs, etc.) reside in the root `assets/` directory, `src/assets` houses the code that manages how these assets are delivered to the user.

## Purpose & Scope

The primary responsibilities of this module are:
- **Dynamic Image Processing**: Converting PNGs to WebP on-the-fly and resizing images based on URL parameters.
- **Caching Strategy**: Setting appropriate cache headers and surrogate keys for assets, especially those with checksums in their URLs.
- **Validation & Maintenance**: Scripts to ensure assets are used correctly, identifying orphaned files, and validating image dimensions.

## Architecture

### Middleware

The core logic resides in `src/assets/middleware`:

- **`dynamic-assets.ts`**: Intercepts requests for `/assets/`. It handles:
  - **WebP Conversion**: If a request ends in `.webp` but the source is a `.png`, it converts the image using `sharp`.
  - **Resizing**: Supports virtual path segments like `/mw-1000/` to resize images to a maximum width (e.g., 1000px).
  - **Security**: Validates requested widths against an allowed list (`VALID_MAX_WIDTHS`) to prevent DoS attacks.
- **`static-asset-caching.ts`**: Detects if an asset URL contains a checksum (e.g., `/assets/cb-12345/...`) and sets aggressive caching headers (`Surrogate-Key: manual-purge`) because the content is immutable.

### Scripts

Located in `src/assets/scripts`, these tools help maintain the asset library:
- `find-orphaned-assets.ts`: Identifies assets present in the disk but not referenced in the content or code.
- `validate-asset-images.ts`: Checks for issues like invalid file types or corruption.
- `list-image-sizes.ts`: Utility for analyzing image dimensions.
