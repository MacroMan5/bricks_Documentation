# Border Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/border-control/](https://academy.bricksbuilder.io/article/border-control/)  
**Last Updated:** 2025-05-22T19:58:15.081Z  
**Extracted:** 2025-05-31 16:56:43

---

# Border Control – Bricks Academy

The border control lets you set the following border properties: 

*   Border width (top/right/bottom/left)
*   Background style (top/right/bottom/left)
*   Background color (none/solid/double/dotted/dashed)
*   Border radius (top/right/bottom/left)

The example below illustrates how to apply a border via the `css` parameter and how to set border defaults.

```
class Builder_Element_Prefix_Test extends \Bricks\Element {
  public function set_controls() {
    $this->controls['titleBorder'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Title border', 'bricks' ),
      'type' => 'border',
      'css' => [
        [
          'property' => 'border',
          'selector' => '.prefix-test-title',
        ],
      ],
      'inline' => true,
      'small' => true,
      'default' => [
        'width' => [
          'top' => 1,
          'right' => 0,
          'bottom' => 0,
          'left' => 0,
        ],
        'style' => 'solid',
        'color' => [
          'hex' => '#ffff00',
        ],
        'radius' => [
          'top' => 1,
          'right' => 1,
          'bottom' => 1,
          'left' => 1,
        ],
      ],


    ];
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
