# Gradient Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/gradient-control/](https://academy.bricksbuilder.io/article/gradient-control/)  
**Last Updated:** 2025-05-22T19:59:58.109Z  
**Extracted:** 2025-05-31 16:56:43

---

# Gradient Control – Bricks Academy

The gradient control lets you define an unlimited number of gradients that you can apply to text, background, and as an overlay.

You can set the CSS selector in the control, adjust the angle between 0 and 360°, and set a color stop for each color.

```
class Prefix_Element_Gradient extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleGradient'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Gradient', 'bricks' ),
      'type' => 'gradient',
      'css' => [
        [
          'property' => 'background-image',
        ],
      ],
    ];
  }

  // Render element HTML
  public function render() {
    echo get_bloginfo( 'name' );
  }
}
```

All sections, rows, columns, and elements already have a **CSS Gradient** control under the Style tab Gradient / Overlay group.

---

*This documentation was extracted from the database for URLs containing 'bricks'*
