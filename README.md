# Advanced-Layout-Builder
Custom Woocommerce Widget is developed for the Advanced Layout Builder. This Widget helps to list the woocommerce products based on product attributes.  Drag and drop the widget and add parameters.

To call the custom widget please add the following code in your theme functions

add_filter('avia_load_shortcodes', 'avia_include_shortcode_template', 15, 1);
function avia_include_shortcode_template($paths) {
  $template_url = get_stylesheet_directory();
  array_unshift($paths, $template_url.'/avia-shortcodes/');
  return $paths;
}
