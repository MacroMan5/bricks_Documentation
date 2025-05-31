# Info Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/info-control/](https://academy.bricksbuilder.io/article/info-control/)  
**Last Updated:** 2025-05-22T19:58:28.716Z  
**Extracted:** 2025-05-31 16:56:43

---

# Info Control – Bricks Academy

The info control does not affect the HTML or CSS on the frontend. It serves as a builder-only helper controls to provide additional information.

Example below: the **Alert** element displays an info control when the _Type_ is set to _Custom_.

```
class Prefix_Element_Info extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['type'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Type', 'bricks' ),
      'type' => 'select',
      'options' => [
        'info' => esc_html__( 'Info', 'bricks' ),
        'success' => esc_html__( 'Success', 'bricks' ),
        'warning' => esc_html__( 'Warning', 'bricks' ),
        'danger' => esc_html__( 'Danger', 'bricks' ),
        'muted' => esc_html__( 'Muted', 'bricks' ),
        'custom' => esc_html__( 'Custom', 'bricks' ),
      ],
      'inline' => true,
      'clearable' => false,
      'pasteStyles' => false,
      'default' => 'info',
    ];

    $this->controls['typeInfo'] = [
      'tab' => 'content',
      'content' => esc_html__( 'Customize alert in STYLE tab.', 'bricks' ),
      'type' => 'info',
      'required' => ['type', '=', 'custom'], // Show info control if 'type' = 'custom'
    ];
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
