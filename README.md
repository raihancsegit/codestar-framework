# Codestar Framework
A Lightweight and easy-to-use WordPress Options Framework. It is a free framework for building theme options. Save your time!

## Screenshot
[![Codestar Framework Screenshot](http://codestarframework.com/assets/images/framework/screenshot.png)](http://codestarframework.com/assets/images/framework/screenshot-1.png)

## [Documentation](http://codestarframework.com/documentation/)
Read the documentation for details [documentation](http://codestarframework.com/documentation/)

## Installation
##### A) Usage as Theme
* Download zip file from github repository
* Extract download zip on `themename/cs-framework` folder under your theme directory
* Add framework include code on your theme `themename/functions.php` file

```php
require_once dirname( __FILE__ ) .'/cs-framework/cs-framework.php';
// -(or)-
require_once get_template_directory() .'/cs-framework/cs-framework.php';
```

* Yay! Right now you are ready to configure framework, metaboxes, taxonomies, wp customize, shortcoder
* Take a look for config files from `themename/cs-framework/config` folder
* Read for more from [documentation](http://codestarframework.com/documentation/)

##### B) Usage as Plugin
* Download zip file from github repository
* **Way1** Extract download zip on `wp-content/plugins/cs-framework` folder under your plugin directory
* **Way2** Upload zip file from `wordpess plugins panel -> add new -> upload plugin`
* Active Codestar Framework plugin from wordpress plugins panel
* Yay! Right now you are ready to configure framework, metaboxes, taxonomies, wp customize, shortcoder
* Take a look for config files from `wp-content/plugins/cs-framework/config` folder also you can manage config files from theme directory. see overriding files method.
* Read for more from [documentation](http://codestarframework.com/documentation/)

## Enable - Disable Mods
Add define code on your `themename/functions.php` directly.
```php
define( 'CS_ACTIVE_FRAMEWORK',   true  ); // default true
define( 'CS_ACTIVE_METABOX',     false ); // default true
define( 'CS_ACTIVE_TAXONOMY',    false ); // default true
define( 'CS_ACTIVE_SHORTCODE',   false ); // default true
define( 'CS_ACTIVE_CUSTOMIZE',   false ); // default true
```
or take a look for change define base code from `/cs-framework/cs-framework.php` directly.

## Enable Light Theme
Add the following define code somewhere in your theme or plugin, and light theme will be active.

```php
define( 'CS_ACTIVE_LIGHT_THEME',  true  ); // default false
```

### Light Theme Screenshot

[![Codestar Framework Screenshot](http://codestarframework.com/assets/images/framework/screenshot-light-1.png)](http://codestarframework.com/assets/images/framework/screenshot-light-1.png)

## Overriding Files
You can override an existing file without change `themename/cs-framework` folder. just create one `themename/cs-framework-override` folder on your theme directory. for eg:

```php
themename/cs-framework-override/config/framework.config.php
themename/cs-framework-override/functions/constants.php
themename/cs-framework-override/fields/text/text.php
```

## Features
- Options Framework
- Metabox Framework
- Taxonomy Framework
- WP Customize Framework
- Shortcode Generator
- Supports Child Themes
- Validate Fields
- Sanitize Fields
- Localization
- Fields Dependencies
- Supports Multilangual Fields
- Reset/Restore/Export/Import Options
- and so much more...

## Options Fields
- Text

	$options[]  = array(
    'name'=> 'footer_section',
    'title'=> 'Footer Section',
    'icon'      => 'fa fa-heart',
    'fields' =>array(
      // begin: a field
        array(
          'id'    => 'unique_text_1',
          'type'  => 'text',
          'title' => 'Text Field',
        ),
        // end: a field

        array(
          'id'    => 'unique_text_2',
          'type'  => 'text',
          'title' => 'Text Field with Description',
          'desc'  => 'Lets write some description for this text field.',
        ),

        array(
          'id'    => 'unique_text_3',
          'type'  => 'text',
          'title' => 'Text Field with Help',
          'help'  => 'I am a Tooltip helper. This field important for something.',
        ),

        array(
          'id'      => 'unique_text_4',
          'type'    => 'text',
          'title'   => 'Text Field with Default',
          'default' => 'some default value bla bla bla',
        ),

        array(
          'id'            => 'unique_text_5',
          'type'          => 'text',
          'title'         => 'Text Field with Placeholder',
          'attributes'    => array(
            'placeholder' => 'do stuff...'
          )
        ),

        array(
          'id'    => 'unique_text_6',
          'type'  => 'text',
          'title' => 'Text Field with After-text',
          'after' => ' <i class="cs-text-muted">( this option is optional )</i>',
        ),

        array(
          'id'     => 'unique_text_7',
          'type'   => 'text',
          'title'  => 'Text Field with Before-text',
          'before' => '<i class="cs-text-muted">( important )</i> ',
        ),

        array(
          'id'    => 'unique_text_8',
          'type'  => 'text',
          'title' => 'Text Field with After-block-text',
          'after' => '<p class="cs-text-info">Information: There is some description for option.</p> ',
        ),

        array(
          'id'         => 'unique_text_9',
          'type'       => 'text',
          'title'      => 'Text Field with Ready-Only',
          'attributes' => array(
            'readonly' => 'only-key'
          ),
          'default'    => 'info@domain.com'
        ),

        array(
          'id'          => 'unique_text_10',
          'type'        => 'text',
          'title'       => 'Text Field with Maxlength (5)',
          'attributes'  => array(
            'maxlength' => '5'
          ),
          'default'     => 'Hello',
        ),

        array(
          'id'         => 'unique_text_11',
          'type'       => 'text',
          'title'      => 'Text Field with Custom Style',
          'attributes' => array(
            'style'    => 'width: 175px; height: 40px; border-color: #93C054;'
          ),
          'after'      => '<p class="cs-text-muted">There is custom css <strong>style="width: 175px; height: 40px; border-color: #93C054;"</strong></p>',
        ),

        array(
          'id'         => 'unique_text_12',
          'type'       => 'text',
          'title'      => 'Text Field with Custom Style',
          'attributes' => array(
            'style'    => 'width: 100%;'
          ),
          'after'      => '<p class="cs-text-muted">There is custom css <strong>style="width: 100%;"</strong></p>'
        ),

        array(
          'id'     => 'unique_text_13',
          'type'   => 'text',
          'before' => '<h4>Text Field without left title</h4>',
          'after'  => '<p class="cs-text-muted">This Text Field do not using left title, just using before text here. also you can remove it.</h4>',
        ),
    )
  );

  return $options;
  
  ########## output ############
	echo cs_get_option('id');
  ########## output ############
  
- Textarea

	$options[]  = array(
		'name'=> 'footer_section',
		'title'=> 'Footer Section',
		'icon'      => 'fa fa-heart',
		'fields' =>array(
		  array(
			  'id'    => 'unique_textarea_1',
			  'type'  => 'textarea',
			  'title' => 'Simple Textarea',
			),

			array(
			  'id'        => 'unique_textarea_1_1',
			  'type'      => 'textarea',
			  'title'     => 'Textarea with Shortcoder',
			  'shortcode' => true,
			),

			array(
			  'id'    => 'unique_textarea_2',
			  'type'  => 'textarea',
			  'title' => 'Textarea Field with Description',
			  'desc'  => 'Lets write some description for this textarea field.',
			),

			array(
			  'id'    => 'unique_textarea_3',
			  'type'  => 'textarea',
			  'title' => 'Textarea Field with Help',
			  'help'  => 'I am a Tooltip helper. This field important for something.',
			),

			array(
			  'id'      => 'unique_textarea_4',
			  'type'    => 'textarea',
			  'title'   => 'Textarea Field with Default',
			  'default' => 'some default value bla bla bla',
			),

			array(
			  'id'            => 'unique_textarea_5',
			  'type'          => 'textarea',
			  'title'         => 'Textarea Field with Placeholder',
			  'attributes'    => array(
				'placeholder' => 'do stuff...'
			  )
			),

			array(
			  'id'    => 'unique_textarea_6',
			  'type'  => 'textarea',
			  'title' => 'Textarea Field with After-text',
			  'after' => '<p class="cs-text-muted">Information: There is some description for option.</p> ',
			),

			array(
			  'id'     => 'unique_textarea_7',
			  'type'   => 'textarea',
			  'title'  => 'Textarea Field with Before-text',
			  'before' => '<p class="cs-text-muted">Information: There is some description for option.</p> ',
			),

			array(
			  'id'         => 'unique_textarea_8',
			  'type'       => 'textarea',
			  'title'      => 'Textarea Field with Before-text',
			  'attributes' => array(
				'rows'     => 10,
			  ),
			  'after'      => '<p class="cs-text-muted">custom textarea attribute rows=10</p> ',
			),

			array(
			  'id'     => 'unique_textarea_13',
			  'type'   => 'textarea',
			  'before' => '<h4>Textarea Field without left title</h4>',
			  'after'  => '<p class="cs-text-muted">This Textarea Field do not using left title, just using before text here. also you can remove it.</h4>',
			),
		)
	  );

	  return $options;
	  
	  ########## output ############
		echo cs_get_option('id');
	  ########## output ############

- Checkbox

	$options[]  = array(
		'name'=> 'footer_section',
		'title'=> 'Footer Section',
		'icon'      => 'fa fa-heart',
		'fields' =>array(
		  array(
			  'id'    => 'unique_checkbox_1',
			  'type'  => 'checkbox',
			  'title' => 'Checkbox',
			  'label' => 'Yes, Please.',
			),

			array(
			  'id'      => 'unique_checkbox_2',
			  'type'    => 'checkbox',
			  'title'   => 'Checkbox with Default Value',
			  'label'   => 'Would you like something ?',
			  'default' => true,
			),

			array(
			  'id'    => 'unique_checkbox_3',
			  'type'  => 'checkbox',
			  'title' => 'Checkbox Field with Help',
			  'label' => 'I am an checkbox',
			  'help'  => 'I am a Tooltip helper. This field important for something.',
			),

			array(
			  'id'       => 'unique_checkbox_4',
			  'type'     => 'checkbox',
			  'title'    => 'Checkbox Field with Options',
			  'options'  => array(
				'blue'   => 'Blue',
				'green'  => 'Green',
				'yellow' => 'Yellow',
			  ),
			),

			array(
			  'id'         => 'unique_checkbox_5',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Options and Default',
			  'options'    => array(
				'bmw'      => 'BMW',
				'mercedes' => 'Mercedes',
				'jaguar'   => 'Jaguar',
			  ),
			  'default'    => 'bmw'
			),

			array(
			  'id'         => 'unique_checkbox_6',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Options Horizontal',
			  'class'      => 'horizontal',
			  'options'    => array(
				'blue'     => 'Blue',
				'green'    => 'Green',
				'yellow'   => 'Yellow',
				'red'      => 'Red',
				'black'    => 'Black',
			  ),
			  'default'    => array( 'green', 'yellow', 'red' )
			),

			array(
			  'id'         => 'unique_checkbox_7',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Pages',
			  'options'    => 'pages',
			),

			array(
			  'id'         => 'unique_checkbox_8',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Posts',
			  'options'    => 'posts',
			),

			array(
			  'id'         => 'unique_checkbox_9',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Categories',
			  'options'    => 'categories',
			),

			array(
			  'id'         => 'unique_checkbox_10',
			  'type'       => 'checkbox',
			  'title'      => 'Checkbox Field with Tags',
			  'options'    => 'tags',
			),

			array(
			  'id'            => 'unique_checkbox_11',
			  'type'          => 'checkbox',
			  'title'         => 'Checkbox Field with Pages',
			  'options'       => 'pages',
			  'query_args'    => array(
				'sort_order'  => 'desc',
				'sort_column' => 'post_title',
			  ),
			  'after'         => '<p class="cs-text-muted"><strong>query_args:</strong> sort_order=desc, sort_column=post_title</p>',
			),

			array(
			  'id'          => 'unique_checkbox_12',
			  'type'        => 'checkbox',
			  'title'       => 'Checkbox Field with CPT Posts',
			  'options'     => 'posts',
			  'query_args'  => array(
				'post_type' => 'your_post_type_name',
			  ),
			  'after'       => '<div class="cs-text-muted"><strong>query_args:</strong> post_type=your_post_type_name</div>',
			),

			array(
			  'id'          => 'unique_checkbox_13',
			  'type'        => 'checkbox',
			  'title'       => 'Checkbox Field with CPT Categories',
			  'options'     => 'categories',
			  'query_args'  => array(
				'type'      => 'your_post_type_name',
				'taxonomy'  => 'your_taxonomy_name',
			  ),
			  'after'       => '<div class="cs-text-muted"><strong>query_args:</strong> post_type=your_post_type_name, taxonomy=your_taxonomy_name</div>',
			),

			array(
			  'id'           => 'unique_checkbox_14',
			  'type'         => 'checkbox',
			  'title'        => 'Checkbox Field with CPT Tags',
			  'options'      => 'tags',
			  'query_args'   => array(
				'taxonomies' => 'your_taxonomy_name',
				'order'      => 'asc',
				'orderby'    => 'name',
			  ),
			  'after'        => '<div class="cs-text-muted"><strong>query_args:</strong> taxonomies=your_taxonomy_name, order=asc, orderby=name</div>',
			),
		)
	  );

	  return $options;
	  
	  ########## output ############
		echo cs_get_option('id');
	  ########## output ############

- Radio
$options[]  = array(
		'name'=> 'footer_section',
		'title'=> 'Footer Section',
		'icon'      => 'fa fa-heart',
		'fields' =>array(
		  array(
          'id'      => 'unique_radio_1',
          'type'    => 'radio',
          'title'   => 'Radio Field',
          'options' => array(
            'yes'   => 'Yes, Please.',
            'no'    => 'No, Thank you.',
          ),
        ),

        array(
          'id'        => 'unique_radio_2',
          'type'      => 'radio',
          'title'     => 'Radio with Default Value',
          'options'   => array(
            'yes'     => 'Yes, Please.',
            'no'      => 'No, Thank you.',
            'nothing' => 'I am not sure, yet!',
          ),
          'default'   => 'nothing',
          'help'      => 'Reference site about Lorem Ipsum, a random Lipsum generator.',
        ),

        array(
          'id'      => 'unique_radio_3',
          'type'    => 'radio',
          'title'   => 'Radio Field',
          'class'   => 'horizontal',
          'options' => array(
            'yes'   => 'Yes, Please.',
            'no'    => 'No, Thank you.',
          ),
          'after'   => '<div class="cs-text-muted">Reference site about Lorem Ipsum, a random Lipsum generator.</div>',
        ),

        array(
          'id'         => 'unique_radio_4',
          'type'       => 'radio',
          'title'      => 'Radio Field with Pages',
          'options'    => 'pages',
        ),

        array(
          'id'         => 'unique_radio_5',
          'type'       => 'radio',
          'title'      => 'Radio Field with Posts',
          'options'    => 'posts',
        ),

        array(
          'id'         => 'unique_radio_6',
          'type'       => 'radio',
          'title'      => 'Radio Field with Categories',
          'options'    => 'categories',
        ),

        array(
          'id'         => 'unique_radio_7',
          'type'       => 'radio',
          'title'      => 'Radio Field with Tags',
          'options'    => 'tags',
        ),

        array(
          'id'            => 'unique_radio_8',
          'type'          => 'radio',
          'title'         => 'Radio Field with Pages',
          'options'       => 'pages',
          'query_args'    => array(
            'sort_order'  => 'desc',
            'sort_column' => 'post_title',
          ),
          'after'         => '<p class="cs-text-muted"><strong>query_args:</strong> sort_order=desc, sort_column=post_title</p>',
        ),

        array(
          'id'          => 'unique_radio_9',
          'type'        => 'radio',
          'title'       => 'Radio Field with CPT Posts',
          'options'     => 'posts',
          'query_args'  => array(
            'post_type' => 'your_post_type_name',
          ),
          'after'       => '<div class="cs-text-muted"><strong>query_args:</strong> post_type=your_post_type_name</div>',
        ),

        array(
          'id'          => 'unique_radio_10',
          'type'        => 'radio',
          'title'       => 'Radio Field with CPT Categories',
          'options'     => 'categories',
          'query_args'  => array(
            'type'      => 'your_post_type_name',
            'taxonomy'  => 'your_taxonomy_name',
          ),
          'after'       => '<div class="cs-text-muted"><strong>query_args:</strong> post_type=your_post_type_name, taxonomy=your_taxonomy_name</div>',
        ),

        array(
          'id'         => 'unique_radio_11',
          'type'       => 'radio',
          'title'      => 'Radio Field',
          'options'    => array(
            'yes'      => 'Yes, Please.',
            'no'       => 'No, Thank you.',
            'nothing'  => 'Nothing.',
          ),
        ),
		)
	  );

	  return $options;
	  
	  ########## output ############
		echo cs_get_option('id');
	  ########## output ############
- Select
- Number
- Icons
- Group
- Image
- Upload
- Gallery
- Sorter
- Wysiwyg
- Switcher
- Background
- Color Picker
- Multi Checkbox
- Checkbox Image Select
- Radio Image Select
- Typography
- Backup
- Heading
- Sub Heading
- Fieldset
- Notice
- and **extendable** fields

## License
Codestar Framework is **free** to use both personal and commercial. If you used commercial, **please credit**.
Read more about GNU [license.txt](http://www.gnu.org/licenses/gpl-2.0.txt)

## Credits
Thanks for guys! Please read [credits](http://codestarframework.com/credits/). If you would like to contribute please fork the project and [report bugs](https://github.com/Codestar/codestar-framework/issues) or submit [pull requests](https://github.com/Codestar/codestar-framework/pulls)</a>.

## The Latest Updates
#### 1.0.2
- Added: Support for WP Nav Menus select
- Added: Taxonomy framework clear form elements after saving
- Added: A filter for external icon-jsons load
- Added: An action `cs_customize_options_config` for customize config options
- Added: Auto Class name for all fields and generating classname by field title
- Added: Chinese language po/mo
- Added: Post type list support
- Added: Typenow param for specific metabox options
- Added: Light theme for framework
- Changed: Action from `cs_validate_save` to `cs_validate_save_after` for save after framework options
- Fixed: Color picker appears twice in widgets
- Fixed: Clear button of color-picker in customizer
- Fixed: Fieldset default value option
- Fixed: Overwrite issue for wp core get_locate() function
- Fixed: Call undefined function wp_get_current_user() issue
- Fixed: Minor bugs
- Updated: Chosen jquery plugin v1.6.1
- Updated: Google Fonts json for Typography field
- Updated: Font Awesome 4.7.0 icons package
- Updated: textdomain updates from __() to esc_html_e() - esc_html__()
- Updated: Backup field idea, changed from base64 encode/decode to seraize/unserialize
- Improved: Icons select field for avoid conflict
- Improved: Locate path function for windows servers
- Improved: Languages packages
- Removed: call_user_function idea
- Removed: custom/callback function support for field options

See [changelog](CHANGELOG.md)

---

##### Using Codestar Framework Themes
[![Route Responsive Multi-Purpose WordPress Theme](http://s3.codestarlive.com/route/userbox/route-preview-promo.png)](http://themeforest.net/item/route-responsive-multipurpose-wordpress-theme/8815770?ref=Codestar)
