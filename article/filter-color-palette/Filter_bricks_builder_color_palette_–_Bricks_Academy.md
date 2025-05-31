# Filter: bricks/builder/color_palette – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/filter-color-palette/](https://academy.bricksbuilder.io/article/filter-color-palette/)  
**Last Updated:** 2025-05-22T19:59:51.606Z  
**Extracted:** 2025-05-31 16:56:43

---

# Filter: bricks/builder/color\_palette – Bricks Academy

Place and customize the following filter to display a different default color palette for the color control.

add\_filter( 'bricks/builder/color\_palette', function( $colors ) {
  // Option #1: Add an individual color
    $colors\[\] \= \[
      'hex' \=> '#3ce77b',
      'rgb' \=> 'rgba(60, 231, 123, 0.56)',
    \];

  // Option #2: Override entire color palette
  $colors \= \[
    \['hex' \=> '#3ce77b'\],
    \['hex' \=> '#f1faee'\],
    \['hex' \=> '#a8dadc'\],
    \['hex' \=> '#457b9d'\],
    \['hex' \=> '#1d3557'\],
  \];

  return $colors;
} );

---

*This documentation was extracted from the database for URLs containing 'bricks'*
