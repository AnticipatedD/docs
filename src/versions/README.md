# Versions

The versions subject handles product versioning for GitHub Docs, including Free/Pro/Team (FPT), Enterprise Cloud (GHEC), and Enterprise Server (GHES). It provides version detection, resolution, feature flags, and version-aware content rendering.

## Purpose & Scope

This subject is responsible for:
- Defining all available product versions (plans and releases)
- Detecting current version from URL paths
- Providing version-aware Liquid conditionals (e.g., `{% if ghes %}`)
- Managing feature flags that vary by version
- Version resolution for content applicability
- Version picker UI component
- Deprecation banners for old versions

Related subjects:
- `src/archives/` - Handles archived versions of documentation
- `src/ghes-releases/` - Manages GHES release and deprecation processes
