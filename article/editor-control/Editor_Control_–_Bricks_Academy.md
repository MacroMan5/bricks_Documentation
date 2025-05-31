# Editor Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/editor-control/](https://academy.bricksbuilder.io/article/editor-control/)  
**Last Updated:** 2025-05-22T19:58:28.902Z  
**Extracted:** 2025-05-31 16:56:43

---

# Editor Control – Bricks Academy

The editor control provides the default WordPress editor. To directly edit content in the builder preview set the `inlineEditing` properties. See the code example below:

```
class Prefix_Element_Editor extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleEditor'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Text editor', 'bricks' ),
      'type' => 'editor',
      'inlineEditing' => [
        'selector' => '.text-editor', // Mount inline editor to this CSS selector
        'toolbar' => true, // Enable/disable inline editing toolbar
      ],
      'default' => esc_html__( 'Here goes the content ..', 'bricks' ),
    ];
  }

  // Render element HTML
  public function render() {
    if ( isset( $this->settings['exampleEditor'] ) ) {
      echo '<div class="text-editor">' . $this->settings['exampleEditor'] . '</div>';
    }
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
