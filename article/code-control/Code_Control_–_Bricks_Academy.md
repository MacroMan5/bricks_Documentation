# Code Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/code-control/](https://academy.bricksbuilder.io/article/code-control/)  
**Last Updated:** 2025-05-22T19:58:35.287Z  
**Extracted:** 2025-05-31 16:56:43

---

# Code Control – Bricks Academy

The code control embeds a code editor utilizing the amazing CodeMirror library. Users for which you’ve enabled “**Code Execution**” in the Bricks settings, will be able to execute PHP, HTML, CSS, and JavaScript.

```
class Prefix_Element_Code extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleHtml'] = [
      'tab' => 'content',
      'label' => esc_html__( 'HTML', 'bricks' ),
      'type' => 'code',
      'mode' => 'php',
      'default' => '<h4>Example H4 HTML title</h4>',
    ];
  }

  // Render element HTML
  public function render() {
    echo isset( $this->settings['exampleHtml'] ) ? $this->settings['exampleHtml'] : esc_html__( 'No HTML provided.', 'bricks' );
  }
}
```

You don’t need to define your own element CSS and JS controls. Those are already available when editing the element under the Style tab “CSS” control group.

---

*This documentation was extracted from the database for URLs containing 'bricks'*
