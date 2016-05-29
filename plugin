<?php
/*
Plugin Name: REST API ALL CORS
Description: Adds CORS headers to allow cross-origin requests to WordPress REST API
Version: 0.0.1
Plugin URI:  http://joshpress.net/access-control-headers-for-the-wordpress-rest-api/
Description: A/B testing made easy for WordPress
Author:    Josh Pollock
Author URI:  http://JoshPress.ney
 */
/**
 * Copyright 2016 Josh Pollock
 *
 * Licensed under the terms of the GNU General Public License version 2 or later
 */
add_action( 'rest_api_init', function() {
    
	remove_filter( 'rest_pre_serve_request', 'rest_send_cors_headers' );
	add_filter( 'rest_pre_serve_request', function( $value ) {
		header( 'Access-Control-Allow-Origin: *' );
		header( 'Access-Control-Allow-Methods: POST, GET, OPTIONS, PUT, DELETE' );
		header( 'Access-Control-Allow-Credentials: true' );

		return $value;
		
	});
}, 15 );
