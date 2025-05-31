# Box Shadow Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/box-shadow-control/](https://academy.bricksbuilder.io/article/box-shadow-control/)  
**Last Updated:** 2025-05-22T19:58:41.916Z  
**Extracted:** 2025-05-31 16:56:43

---

# Box Shadow Control – Bricks Academy

The box-shadow control is a CSS control and you can set the following properties:

*   Offset X
*   Offset Y
*   Spread
*   Blur
*   Color
*   Inset

```
class Prefix_Element_Box_Shadow extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleBoxShadow'] = [
      'tab' => 'content',
      'label' => esc_html__( 'BoxShadow', 'bricks' ),
      'type' => 'box-shadow',
      'css' => [
        [
          'property' => 'box-shadow',
          'selector' => '.prefix-box-shadow-wrapper',
        ],
      ],
      'inline' => true,
      'small' => true,
      'default' => [
        'values' => [
          'offsetX' => 0,
          'offsetY' => 0,
          'blur' => 2,
          'spread' => 0,
        ],
        'color' => [
          'rgb' => 'rgba(0, 0, 0, .1)',
        ],
      ],
    ];
  }

  // Render element HTML
  public function render() {
    echo '<div class="prefix-box-shadow-wrapper">';
    echo get_bloginfo( 'name' );
    echo '</div>';
  }
}
```

### Resources

[https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow](https://developer.mozilla.org/en-US/docs/Web/CSS/box-shadow)

---

*This documentation was extracted from the database for URLs containing 'bricks'*
