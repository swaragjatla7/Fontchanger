# Fontchanger
To edit fonts on the theme
=== Fontchanger - Custom Fonts and Colors ===
Tags: customizer, css, color, colors, colour, colours, fonts, google fonts, localize, localization

Fontchanger allows you to customize fonts and colors in WordPress themes through the Customizer - no need of any additional code!

== Description ==
Without any additional code Fontc ahnger allows you to customise the WordPress themes by Customisable option!
Using wordpress Customiser font can be edited easily. When desired font and colour is selected preview is seen.
Fontchanger allows to change font colour and font style gives a unique style to website.
Default WordPress themes are fully supported and support for more themes can be added in the future. All other themes can be customized into desired fontstyle.
Fontchanger uses Google fonts. This helps to give various font styles and colours to personalise the website

= Features =

* Choose from a varied selection of the top Google fonts in any theme
* Additional themes (listed below) support editing colors
* Developer functionality for adding support to other themes, and for adding additional fonts.

= Supported Character Sets =

Fontchanger supports fonts that have a variety of different character sets. This makes selecting a font for your language super easy. The supported character sets are:

Cyrillic,Devanagari,Greek,Hebrew,Latin, Vietnamese

* Supported Themes *

Most of the Wordpress default themes

Developers can add support for their themes quite easily - see the 'Other Notes' tab for more info.

== How To ==

After downloading and installing the plugin you can go to the Customizer (Appearance > Customizer) and edit fonts and colors in the 'Colors & Fonts' panel.

= Adding Theme Support =

Fontchanger allows any theme to add support through the `add_theme_support` command. For examples check out the theme-styles directory.

I have added an example of a basic implementation below. This code would be placed in your themes functions.php

`function prefix_add_Fontchanger_support() {

  $properties = array(
	...
  );
  add_theme_support( 'Fontchanger', $properties );

}

add_filter( 'after_setup_theme', 'prefix_add_Fontchanger_support' );`

= Extra Fonts =

Fontchanger currently offers developers a filter for adding additional fonts. You can use it as shown below

`function my_fonts( $font_list ) {
	$font_list['Cormorant Infant'] = array(
		'name' => 'Cormorant Infant',
		'family' => '"Cormorant Infant", serif',
		'weight' => '400,700',
		'sets' => array( 'latin' ),
	);
	$font_list['Poppins'] = array(
		'name' => 'Poppins',
		'family' => 'Poppins, sans-serif',
		'weight' => '400,700',
		'sets' => array( 'latin' ),
	);
	return $font_list;
}
add_filter( 'Fontchanger_get_fonts', 'my_fonts' );`

*Version*
= 1.0 =
* first version
