# Color Schemes

This module manages the application of color themes (light, dark, high contrast, etc.) to the GitHub Docs site. It ensures that the documentation matches the user's preferred color scheme as configured on GitHub.com.

## Purpose & Scope

The primary goal is to read the user's color preference from a cookie and apply the correct theme context to the React application. This supports:
- **Modes**: Light, Dark, Auto (system preference).
- **Themes**: Specific variations like "Dark Dimmed" or "Dark High Contrast".
- **Compatibility**: Bridging the gap between raw CSS class names and Primer React component props.

  - *Reference*: [Primer React Issue #2229](https://github.com/primer/react/issues/2229)
- **Future**: The long-term goal is to rely entirely on CSS variables, removing the need for complex JavaScript state management for theming.
