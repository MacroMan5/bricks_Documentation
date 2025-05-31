# Query Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/query-control/](https://academy.bricksbuilder.io/article/query-control/)  
**Last Updated:** 2025-05-22T19:59:58.387Z  
**Extracted:** 2025-05-31 16:56:43

---

# Query Control – Bricks Academy

The query control lets you set query arguments to retrieve items of any post type. Use the returned value to set up a custom `WP_Query` to render the matching posts in any way you want.

```
class Prefix_Element_Posts extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['exampleQueryArgs'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Posts', 'bricks' ),
      'type' => 'query',
      // Default required for query to populate
      'default' => [
        'post_type' => 'post',
      ],
    ];
  }

  // Render element HTML
  public function render() {
    $query_args = $this->settings['exampleQueryArgs'];
    $posts_query = new WP_Query( $query_args );

    // Standard WordPress loop
    if ( $posts_query->have_posts() ) :
      while ( $posts_query->have_posts() ) : $posts_query->the_post();
        // Render post title and thumbnail
        the_title( '<h5>', '</h5>' );
        the_post_thumbnail( 'thumbnail' );
      endwhile;

      wp_reset_postdata();
    else :
     esc_html_e( 'No posts matched your criteria.', 'bricks' );
    endif;
  }
}
```

### Resources

*   [https://codex.wordpress.org/Class\_Reference/WP\_Query#Parameters](https://codex.wordpress.org/Class_Reference/WP_Query#Parameters)

---

*This documentation was extracted from the database for URLs containing 'bricks'*
