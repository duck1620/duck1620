<?php
/**
 * willgroup functions and definitions.
 *
 * @link https://developer.wordpress.org/themes/basics/theme-functions/
 *
 * @package willgroup
 */

if ( ! function_exists( 'willgroup_setup' ) ) :
/**
 * Sets up theme defaults and registers support for various WordPress features.
 *
 * Note that this function is hooked into the after_setup_theme hook, which
 * runs before the init hook. The init hook is too late for some features, such
 * as indicating support for post thumbnails.
 */
function willgroup_setup() {
	/*
	 * Make theme available for translation.
	 * Translations can be filed in the /languages/ directory.
	 * If you're building a theme based on willgroup, use a find and replace
	 * to change 'willgroup' to the name of your theme in all the template files.
	 */
	load_theme_textdomain( 'willgroup', get_template_directory() . '/languages' );

	// Add default posts and comments RSS feed links to head.
	add_theme_support( 'automatic-feed-links' );

	/*
	 * Let WordPress manage the document title.
	 * By adding theme support, we declare that this theme does not use a
	 * hard-coded <title> tag in the document head, and expect WordPress to
	 * provide it for us.
	 */
	add_theme_support( 'title-tag' );

	/*
	 * Enable support for Post Thumbnails on posts and pages.
	 *
	 * @link https://developer.wordpress.org/themes/functionality/featured-images-post-thumbnails/
	 */
	add_theme_support( 'post-thumbnails' );

	// This theme uses wp_nav_menu() in one location.
	register_nav_menus( array(
		'site-navigation'     => esc_html__( 'Site navigation', 'willgroup' ),
		'sidebar-menu' 	      => esc_html__( 'Sidebar menu', 'willgroup' ),
		'footer-nav-1' 	  	  => esc_html__( 'Footer navigation 1', 'willgroup' ),
		'footer-nav-2' 	      => esc_html__( 'Footer navigation 2', 'willgroup' ),
		'footer-nav-3' 	      => esc_html__( 'Footer navigation 3', 'willgroup' ),
		'footer-nav-4' 	      => esc_html__( 'Footer navigation 4', 'willgroup' ),
		'footer-nav-5' 	      => esc_html__( 'Footer navigation 5', 'willgroup' ),
	) );

	/*
	 * Switch default core markup for search form, comment form, and comments
	 * to output valid HTML5.
	 */
	add_theme_support( 'html5', array(
		'search-form',
		'comment-form',
		'comment-list',
		'gallery',
		'caption',
	) );

	/*
	 * Add image sizes
	 */
	add_image_size( '70x70', 70, 70, true );
}
endif;
add_action( 'after_setup_theme', 'willgroup_setup' );

/**
 * Remove medium_large size
 */
function willgroup_remove_image_sizes( $sizes) {
	unset( $sizes['thumbnail'] );
	unset( $sizes['medium'] );
	unset( $sizes['medium_large'] );
	unset( $sizes['large'] );
	return $sizes;
}
add_filter('intermediate_image_sizes_advanced', 'willgroup_remove_image_sizes');

/**
 * Set the content width in pixels, based on the theme's design and stylesheet.
 *
 * Priority 0 to make it available to lower priority callbacks.
 *
 * @global int $content_width
 */
function willgroup_content_width() {
	$GLOBALS['content_width'] = apply_filters( 'willgroup_content_width', 640 );
}
add_action( 'after_setup_theme', 'willgroup_content_width', 0 );

/**
 * Enqueue scripts and styles.
 */
function willgroup_scripts() {
	wp_enqueue_style( 'willgroup-bootstrap-css', get_template_directory_uri() . '/css/bootstrap.min.css' );
	
	wp_enqueue_style( 'willgroup-bootstrap-datetimepicker-css', get_template_directory_uri() . '/css/bootstrap-datetimepicker.css' );
	
	wp_enqueue_style( 'willgroup-icon', get_template_directory_uri() . '/css/font-awesome.min.css' );
		
	wp_enqueue_style( 'willgroup-animate', get_template_directory_uri() . '/css/animate.css' );
	
	wp_enqueue_style( 'willgroup-owl-carousel-css', get_template_directory_uri() . '/css/owl.carousel.css' );
	
	wp_enqueue_style( 'willgroup-style', get_stylesheet_uri() );

	wp_enqueue_script( 'willgroup-skip-link-focus-fix', get_template_directory_uri() . '/js/skip-link-focus-fix.js', array(), '', true );
	
	wp_enqueue_script( 'willgroup-tether', get_template_directory_uri() . '/js/tether.min.js', array(), '', true );
	
	wp_enqueue_script( 'willgroup-bootstrap-js', get_template_directory_uri() . '/js/bootstrap.min.js', array( 'jquery' ), '', true );
	
	wp_enqueue_script( 'willgroup-moment-js', get_template_directory_uri() . '/js/moment.js', array( 'jquery' ), '', true );
	
	wp_enqueue_script( 'willgroup-vi-js', get_template_directory_uri() . '/js/vi.js', array( 'jquery' ), '', true );
	
	wp_enqueue_script( 'willgroup-bootstrap-datetimepicker-js', get_template_directory_uri() . '/js/bootstrap-datetimepicker.min.js', array( 'jquery' ), '', true );
				
	wp_enqueue_script( 'willgroup-owl-carousel-js', get_template_directory_uri() . '/js/owl.carousel.min.js', array( 'jquery' ), '', true );
	
	wp_enqueue_script( 'willgroup-site', get_template_directory_uri() . '/js/site.js', array( 'jquery' ), '', true );

	if ( is_singular() && comments_open() && get_option( 'thread_comments' ) ) {
		wp_enqueue_script( 'comment-reply' );
	}
}
add_action( 'wp_enqueue_scripts', 'willgroup_scripts' );

/**
 * Bfi thumb
 */
require get_template_directory() . '/inc/bfi_thumb/BFI_Thumb.php';

/**
 * Post
 */
require get_template_directory() . '/inc/post.php';
require get_template_directory() . '/inc/page.php';
require get_template_directory() . '/inc/consultant.php';
require get_template_directory() . '/inc/call.php';

/**
 * Register widget area.
 */
require get_template_directory() . '/inc/widgets.php';
require get_template_directory() . '/inc/widgets/widget-service.php';
require get_template_directory() . '/inc/widgets/widget-support.php';
require get_template_directory() . '/inc/widgets/widget-making-appt.php';
require get_template_directory() . '/inc/widgets/widget-popular-posts.php';
require get_template_directory() . '/inc/widgets/widget-category-posts.php';
require get_template_directory() . '/inc/widgets/widget-categories.php';

/**
 * Ajax functions
 */
require get_template_directory() . '/inc/ajax.php';

/**
 * Theme Customizer.
 */
require get_template_directory() . '/inc/redux-framework/ReduxCore/framework.php';
require get_template_directory() . '/inc/customizer.php';

/**
 * Load Breadcrumb
 */
require get_template_directory() . '/inc/breadcrumb.php';

/**
 * Load Pagination
 */
require get_template_directory() . '/inc/pagination.php';

/**
 * Truncate text.
 */
function truncate($text, $chars = 120) {
	$text = wp_strip_all_tags( $text );
    $text = $text." ";
    $text = substr($text,0,$chars);
    $text = substr($text,0,strrpos($text,' '));
    $text = $text."...";
    return $text;
}

/**
 * Resize image.
 */
function resize_image( $image_width, $image_height, $post_id = '' ) {
	if ( $post_id ) {
		$params = array( 'width' => $image_width, 'height' => $image_height );
		$imgsrc = wp_get_attachment_image_src( get_post_thumbnail_id( $post_id, '' ), 'full' );
		$custom_img_src = bfi_thumb( $imgsrc[0], $params );
		return $custom_img_src;
	} else {
		global $post;
		$params = array( 'width' => $image_width, 'height' => $image_height );
		$imgsrc = wp_get_attachment_image_src( get_post_thumbnail_id( $post->ID, '' ), 'full' );
		$custom_img_src = bfi_thumb( $imgsrc[0], $params );
		return $custom_img_src;
	}
}

/**
 * Query post tags
 */
function willgroup_query_post_tags( $where ) {
	$where = str_replace("meta_key = 'post_tags_%", "meta_key LIKE 'post_tags_%", $where);
	return $where;
}
add_filter('posts_where', 'willgroup_query_post_tags');

/**
 * Query page tags
 */
function willgroup_query_page_tags( $where ) {
	$where = str_replace("meta_key = 'page_tags_%", "meta_key LIKE 'page_tags_%", $where);
	return $where;
}
add_filter('posts_where', 'willgroup_query_page_tags');

/**
 * Insert banner in the Middle of a Post
 */
function willgroup_ad_content( $content ) {
    if( is_single() || is_page() ) {
		global $willgroup_customize;
		$content.= '<div class="hotline">';
		$content.= '<img src="' . get_template_directory_uri() . '/images/bg-hotline.png"/>';
		$content.= '<a href="' . $willgroup_customize['hotline_link_1'] . '"><img class="image-1" src="' . get_template_directory_uri() . '/images/btn-hotline-1.png"/></a>';
		$content.= '<a href="' . $willgroup_customize['hotline_link_2'] . '"><img class="image-2" src="' . get_template_directory_uri() . '/images/btn-hotline-2.png"/></a>';
		$content.= '<a href="' . $willgroup_customize['hotline_link_3'] . '"><img class="image-3" src="' . get_template_directory_uri() . '/images/btn-hotline-3.png"/></a>';
		$content.= '</div>';
		return $content;
	}
}
add_filter('the_content', 'willgroup_ad_content');
/**
 * vidoe
 */
add_shortcode( 'shortcode_video_gallery', 'create_shortcode_album' );
function create_shortcode_album( $atts ) {
    ob_start();
    $query = new WP_Query( array(
        'post_type' => 'video',
		'showposts' => 10 
    ) );
    if ( $query->have_posts() ) { ?>
        <section class="tt-video">
			<div class="container">
				<h2 class="module-title"><i class="icon icon-medkit"></i>Video</h2>
				<div class="row">
					<?php while (have_posts()) : the_post(); ?>
					<div class="col-md-6">
						<div class="tt-video-item">
							<?php the_field('link_video'); ?>					
						</div>
					</div>
					<?php endwhile;?>
				</div>
			</div>
	</section>
    <?php $myvariable = ob_get_clean();
    return $myvariable;
    }
}
