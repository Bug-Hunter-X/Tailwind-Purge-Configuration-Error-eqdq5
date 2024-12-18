# Tailwind CSS Purge Configuration Error

This repository demonstrates a common error encountered when using Tailwind CSS's purge feature.  Incorrectly configuring the `purge` option can lead to the unexpected removal of styles from your production build, resulting in broken styles.

## Bug Report
The issue stems from an empty `purge` array in the `tailwind.config.js` file. This instructs Tailwind to remove *all* unused styles, regardless of whether they're actually needed.  This will almost certainly break your styling.

## Solution
The solution is to correctly configure the `purge` option to specify the files or patterns that Tailwind should scan for used styles.  This ensures that only unused styles are removed.

Refer to the `tailwind.config.solution.js` for the corrected configuration.  This example uses the glob pattern to include all files in the `src` directory. This may need adjustment based on your project structure.