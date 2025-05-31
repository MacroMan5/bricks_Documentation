# Checkbox Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/checkbox-control/](https://academy.bricksbuilder.io/article/checkbox-control/)  
**Last Updated:** 2025-05-22T19:58:28.698Z  
**Extracted:** 2025-05-31 16:56:43

---

# Checkbox Control – Bricks Academy

The checkbox control is a simple on/off switch. If enabled it outputs a boolean value of `true`. Disabled it returns `false`. You can use it to conditionally show/hide other content settings as we illustrate in the following code example:

class Prefix\_Element\_Checkbox extends \\Bricks\\Element {
  // Set builder controls
  public function set\_controls() {
    $this\->controls\['exampleCheckbox'\] \= \[
      'tab' \=> 'content',
      'label' \=> esc\_html\_\_( 'Show site title', 'bricks' ),
      'type' \=> 'checkbox',
      'inline' \=> true,
      'small' \=> true,
      'default' \=> true, // Default: false
    \];
  }

  // Render element HTML
  public function render() {
    // Show site title if setting checkbox 'exampleCheckbox' is checked
    if ( isset( $this\->settings\['exampleCheckbox'\] ) ) {
      echo get\_bloginfo( 'name' );
    }
  }
}

---

*This documentation was extracted from the database for URLs containing 'bricks'*
