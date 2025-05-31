# Element Controls – Bricks Academy

**Source URL:** [https://academy.bricksbuilder.io/article/element-controls/](https://academy.bricksbuilder.io/article/element-controls/)  
**Last Updated:** 2025-05-22T19:59:51.288Z  
**Extracted:** 2025-05-31 16:56:43

---

# Element Controls – Bricks Academy

Element controls allow the user to change the content and appearance of an element. You can define the controls of an element with the set\_controls() method in your [element PHP class](https://academy.bricksbuilder.io/article/create-your-own-elements/).

Example element class with control parameters for control `testColor`:

class Prefix\_Element\_Test extends \\Bricks\\Element {
  public function set\_controls() {
    $this\->controls\['testColor'\] \= \[
      'tab' \=> 'content',
      'group' \=> 'settings',
      'label' \=> esc\_html\_\_( 'Text color', 'bricks' ),
      'type' \=> 'color',
      'inline' \=> true,
      'small' \=> true,
      'css' \=> \[
        \[
          'property' \=> 'color',
          'selector' \=> '.content',
          'important' \=> true, // Optional
        \],
      \],
      'default' \=> \[
        'rgb' \=> 'rgba(158, 158, 158, .8)',
        'hex' \=> '#9e9e9e',
      \],
      'pasteStyles' \=> false,
      'description' \=> esc\_html\_\_( 'Define the content color.', 'bricks' ),
      'required' \=> \['showText', '!=', ''\],
    \];
  }
}

The following control parameters are available for all control types. To dive deeper into the arguments of a specific control type select the control from the list at the bottom.

### Universal control arguments

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| tab | string | content | Tab under which to show the control. Accepts: `content` or `style`. |
| group | string |     | Group under which to show the control. By default a control shows ungrouped under the `content` tab. |
| label | string |     | Localized control label. E.g.: `esc_html__( 'Color', 'bricks' ),` |
| type | string |     | Set the control type (see the list below for a list of all available control types). |
| inline | bool | false | Set to true to show control label and input on the same line. |
| small | bool | false | Set to true to show a control input of 60px width. By default inline label and input have equal widths of 50%. |
| css | array |     | Array with CSS rule definitions. Each CSS rule is a separate array and requires a `property` and `selector` parameter. |
| default | string/array |     | Default control value. Either a string or an array (depending on the control type, see control list below for specific control default) |
| pasteStyles | bool | true | Set to true excludes setting from being pasted via the builders’ custom right click “Paste Styles”. Recommended for all controls that output HTML content instead of CSS. |
| description | string |     | Optional description for controls that need additional explanation or link to a resource. |
| required | array |     | Show control in relation to the setting of another control.<br><br>Parameter #1: control ID  <br>Parameter #2: comparison operator:  `=`, `!=`, `>=`, `<=`  <br>Parameter #3: setting value<br><br>Example: `'required' => ['layout', '=', ['list', 'grid']],`  <br>Required condition: Show this control if setting value of control `layout` equals `=` either `list` or `grid`. |

### Controls Types

| Control Type | Output (Content/CSS) |
| --- | --- |
| [apply](https://academy.bricksbuilder.io/article/apply-control/) | None |
| [align-items](https://academy.bricksbuilder.io/article/align-items-control/) | CSS |
| [audio](https://academy.bricksbuilder.io/article/audio-control/) | Content |
| [background](https://academy.bricksbuilder.io/article/background-control/) | CSS |
| [border](https://academy.bricksbuilder.io/article/border-control/) | CSS |
| [box-shadow](https://academy.bricksbuilder.io/article/box-shadow-control/) | CSS |
| [checkbox](https://academy.bricksbuilder.io/article/checkbox-control/) | Conditional |
| [code](https://academy.bricksbuilder.io/article/code-control/) | Content |
| [color](https://academy.bricksbuilder.io/article/color-control/) | CSS |
| [datepicker](https://academy.bricksbuilder.io/article/datepicker-control/) | Content |
| [dimensions](https://academy.bricksbuilder.io/article/dimensions-control/) | CSS |
| [direction](https://academy.bricksbuilder.io/article/direction-control/) | CSS |
| [editor](https://academy.bricksbuilder.io/article/editor-control/) | Content |
| [filters](https://academy.bricksbuilder.io/article/filters-control/) | CSS |
| [gradient](https://academy.bricksbuilder.io/article/gradient-control/) | CSS |
| [icon](https://academy.bricksbuilder.io/article/icon-control/) | Content |
| [image](https://academy.bricksbuilder.io/article/image-control/) | Content/CSS |
| [image-gallery](https://academy.bricksbuilder.io/article/image-gallery-control/) | Content |
| [info](https://academy.bricksbuilder.io/article/info-control/) | Builder panel only |
| [justify-content](https://academy.bricksbuilder.io/article/justify-content-control/) | CSS |
| [link](https://academy.bricksbuilder.io/article/link-control/) | Content |
| [number](https://academy.bricksbuilder.io/article/number-control/) | Content/CSS |
| [posts](https://academy.bricksbuilder.io/article/posts-control/) | Content |
| [repeater](https://academy.bricksbuilder.io/article/repeater-control/) | Content |
| [select](https://academy.bricksbuilder.io/article/select-control/) | Content/CSS |
| [slider](https://academy.bricksbuilder.io/article/slider-control/) | Content |
| [svg](https://academy.bricksbuilder.io/article/svg-control/) | Content |
| [text](https://academy.bricksbuilder.io/article/text-control/) | Content |
| [textarea](https://academy.bricksbuilder.io/article/textarea-control/) | Content |
| [text-align](https://academy.bricksbuilder.io/article/text-align-control/) | CSS |
| [text-decoration](https://academy.bricksbuilder.io/article/text-decoration-control/) | CSS |
| [text-shadow](https://academy.bricksbuilder.io/article/text-shadow-control/) | CSS |
| [text-transform](https://academy.bricksbuilder.io/article/text-transform-control/) | CSS |
| [typography](https://academy.bricksbuilder.io/article/typography-control/) | CSS |

---

*This documentation was extracted from the database for URLs containing 'bricks'*
