# Audio Control – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/audio-control/](https://academy.bricksbuilder.io/article/audio-control/)  
**Last Updated:** 2025-05-22T19:58:42.316Z  
**Extracted:** 2025-05-31 16:56:43

---

# Audio Control – Bricks Academy

The audio control lets you select an audio file from the media library. It also gives you various options to show/hide artist and title, choose between a light/dark theme, autoplay the audio file, etc. It has no custom control parameters.

```
class Prefix_Element_Audio extends \Bricks\Element {
  // Set builder controls
  public function set_controls() {
    $this->controls['file'] = [
      'tab' => 'content',
      'label' => esc_html__( 'Audio file', 'bricks' ),
      'type' => 'audio',
    ];
  }

  // Render element HTML
  public function render() {
    $settings = $this->settings;

    if ( isset( $settings['file']['url'] ) ) {
      echo wp_audio_shortcode( [
        'src'      => $settings['file']['url'],
        'loop'     => isset( $settings['loop'] ) ? $settings['loop'] : false, 
        'autoplay' => isset( $settings['autoplay'] ) ? $settings['autoplay'] : false, 
        'preload'  => isset( $settings['preload'] ) ? $settings['preload'] : 'none', 
      ] );
    }
  }
}
```

### Resources

[https://codex.wordpress.org/Function\_Reference/wp\_audio\_shortcode](https://codex.wordpress.org/Function_Reference/wp_audio_shortcode)

---

*This documentation was extracted from the database for URLs containing 'bricks'*
