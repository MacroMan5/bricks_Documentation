# Filter: bricks/builder/i18n – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/filter-bricks-i18n/](https://academy.bricksbuilder.io/article/filter-bricks-i18n/)  
**Last Updated:** 2025-05-22T19:59:55.792Z  
**Extracted:** 2025-05-31 16:56:43

---

# Filter: bricks/builder/i18n – Bricks Academy

Place and customize the following filter to add translatable string to the builder.

add\_filter( 'bricks/builder/i18n', function( $i18n ) {
  // Example: Provide translatable string for element category 'custom'
  $i18n\['custom'\] \= esc\_html\_\_( 'Custom', 'bricks' );

  return $i18n;
} );

---

*This documentation was extracted from the database for URLs containing 'bricks'*
