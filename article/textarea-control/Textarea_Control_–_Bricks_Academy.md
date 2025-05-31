# Textarea Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/textarea-control/](https://academy.bricksbuilder.io/article/textarea-control/)  
**Last Updated:** 2025-05-22T19:58:37.266Z  
**Extracted:** 2025-05-31 16:56:43

---

# Textarea Control – Bricks Academy

The textarea control displays a textarea input field. You can set the following parameters:

*   `rows` (number. Default: 5)
*   `readonly` (true/false. Default: false)
*   `spellcheck` (true/false. Default: false)
*   `inlineEditing` (true to enable)

```
class Prefix_Element_Textarea extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleTextarea'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Textarea', 'bricks' ),
      'type' => 'textarea',
      // 'readonly' => true, // Default: false
      'rows' => 10, // Default: 5
      'spellcheck' => true, // Default: false
      'inlineEditing' => true,
      'default' => 'Here goes your content ..',
    ];
  }

  // Render element HTML
  public function render() {
    if ( isset( $this->settings['exampleTextarea'] ) ) {
      echo $this->settings['exampleTextarea'];
    } else {
      esc_html_e( 'No text provided.', 'bricks' );
    }
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
