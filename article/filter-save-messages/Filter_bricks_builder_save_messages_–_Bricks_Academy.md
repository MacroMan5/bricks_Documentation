# Filter: bricks/builder/save_messages – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/filter-save-messages/](https://academy.bricksbuilder.io/article/filter-save-messages/)  
**Last Updated:** 2025-05-22T19:58:15.131Z  
**Extracted:** 2025-05-31 16:56:43

---

# Filter: bricks/builder/save\_messages – Bricks Academy

Place and customize the following filter to display different save message every time you manually save your progress when editing with Bricks.

add\_filter( 'bricks/builder/save\_messages', function( $messages ) {
  // Option #1: Append individual save message to existing message collection
    $messages\[\] \= 'Yasss';

  // Option #2: Replace all existing builder save messages
    $messages \= \[
      'Done',
      'Cool',
      'High five!',
    \];

  return $messages;
} );

---

*This documentation was extracted from the database for URLs containing 'bricks'*
