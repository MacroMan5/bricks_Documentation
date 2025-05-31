# Filter: bricks/builder/standard_fonts – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/filter-standard-fonts/](https://academy.bricksbuilder.io/article/filter-standard-fonts/)  
**Last Updated:** 2025-05-22T19:59:51.796Z  
**Extracted:** 2025-05-31 16:56:43

---

# Filter: bricks/builder/standard\_fonts – Bricks Academy

Place and customize the following filter to display a different set of web-safe fonts in the typography control.

add\_filter( 'bricks/builder/standard\_fonts', function( $standard\_fonts ) {
  // Option #1: Add individual standard font
  $standard\_fonts\[\] \= 'Verdana';

  // Option #2: Replace all standard fonts
  $standard\_fonts \= \[
    'Georgia',
    'Times New Roman',
    'Verdana',
  \];

  return $standard\_fonts;
} );

---

*This documentation was extracted from the database for URLs containing 'bricks'*
