# Number Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/number-control/](https://academy.bricksbuilder.io/article/number-control/)  
**Last Updated:** 2025-05-22T19:58:35.819Z  
**Extracted:** 2025-05-31 16:56:43

---

# Number Control – Bricks Academy

The number control represents a simple number input field. It has the following custom properties:

*   units (optional: boolean or array)
*   unit (string: `px`, `em`, `rem` etc.)
*   min (number)
*   step (Default: 1) (Custom: ‘0.1’ etc.)

Use it to render a number to the page or set the `css` control property to target a specific CSS style.

```
class Prefix_Element_Number extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleNumber'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Number', 'bricks' ),
      'type' => 'number',
      'min' => 0,
      'step' => '0.1', // Default: 1
      'inline' => true,
      'default' => 123,
    ];

    $this->controls['examplePadding'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Padding in px', 'bricks' ),
      'type' => 'number',
      'unit' => 'px',
      'inline' => true,
      'css' => [
        [
          'property' => 'padding',
        ],
      ],
      'default' => 33,
    ];
  }

  // Render element HTML
  public function render() {
    if ( isset( $this->settings['exampleNumber'] ) ) {
      echo esc_html__( 'Number: ', 'bricks' ) . $this->settings['exampleNumber'];
    } else {
      esc_html_e( 'No number provided.', 'bricks' );
    }
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
