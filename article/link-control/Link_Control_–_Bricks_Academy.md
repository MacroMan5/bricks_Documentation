# Link Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/link-control/](https://academy.bricksbuilder.io/article/link-control/)  
**Last Updated:** 2025-05-22T19:58:35.692Z  
**Extracted:** 2025-05-31 16:56:43

---

# Link Control – Bricks Academy

The link control give you the choice of different link types:

*   Internal post/page
*   External URL
*   Popup (image, video)

```
class Prefix_Element_Link extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleLink'] = [
      'tab'         => 'content',
      'label'       => esc_html__( 'Link', 'bricks' ),
      'type'        => 'link',
      'pasteStyles' => false,
      'placeholder' => esc_html__( 'http://yoursite.com', 'bricks' ),
      // 'exclude'     => [
      //  'rel',
      //  'newTab',
      // ],
    ];
  }

  // Render element HTML
  public function render() {
    if ( isset( $this->settings['exampleLink'] ) ) {
      // Set link attributes by passing attribute key and link settings
      $this->set_link_attributes( 'a', $this->settings['exampleLink'] );

      echo '<a ' . $this->render_attributes( 'a' ) . '>' . get_bloginfo( 'name' ) . '</a>';
    } else {
      esc_html_e( 'No link provided.', 'bricks' );
    }
  }
}
```

---

*This documentation was extracted from the database for URLs containing 'bricks'*
