/*

Theme Name: Will Group

Theme URI: http://willgroup.net/

Author: Vo Vuong

Author URI: http://willgroup.net/

Description: One for All from Will Group

Version: 1.0.0

License: GNU General Public License v2 or later

License URI: http://www.gnu.org/licenses/gpl-2.0.html

Text Domain: willgroup

Tags:



This theme, like WordPress, is licensed under the GPL.

Use it to make something cool, have fun, and share what you've learned with others.

*/



/*--------------------------------------------------------------

>>> TABLE OF CONTENTS:

----------------------------------------------------------------

# Normalize

# Typography

# Elements

# Forms

# Navigation

	## Links

	## Menus

# Accessibility

# Alignments

# Clearings

# Widgets

# Content

	## Posts and pages

	## Comments

# Infinite scroll

# Media

	## Captions

	## Galleries

--------------------------------------------------------------*/
@import url('https://fonts.googleapis.com/css?family=Open+Sans');


@font-face {

    font-family: 'UTM Bebas';

    font-style: normal;

    font-weight: 400;

    src: url("fonts/UTM Bebas.eot?#iefix") format("embedded-opentype"), 

		 url("fonts/UTM Bebas.woff") format("woff"), 

		 url("fonts/UTM Bebas.ttf") format("truetype"), 

		 url("fonts/UTM Bebas.otf") format("opentype");

}

.row-small {

	margin-left: -0.5rem;

	margin-right: -0.5rem;

}

.col-small {

	padding-left: 0.5rem;

	padding-right: 0.5rem;

}

@media (max-width: 767px) {

	html {

		font-size: 14px;

	}

	.row {

		margin-left: -8px;

		margin-right: -8px;

	}

	.container,

	[class*='col-'] {

		padding-left: 8px;

		padding-right: 8px;

	}

}



/*--------------------------------------------------------------

# Global

--------------------------------------------------------------*/

body {

	font-family: 'Open Sans',sans-serif !important;

	font-size: 0.9875rem;

	font-weight: 400;

	color: #555;

}

* {

	outline: none !important;

}

img {

	max-width: 100%;

	height: auto;

}

.inline-block {

	float: none;

	display: inline-block;

	vertical-align: top;

	margin-right: -4px;

}

.img-rounded {

	border: 2px solid #ddd;

	-webkit-border-radius: 0.5rem;

	-moz-border-radius: 0.5rem;

	border-radius: 0.5rem;

}

.img-circle {

	border: 2px solid #ddd;

}

a {

	text-decoration: none;

	color: #555;

	-webkit-transition: all 200ms ease 0s;

	-moz-transition: all 200ms ease 0s;

	transition: all 200ms ease 0s;

}

a:hover,

a:focus {

	text-decoration: none;

	color: #F22A70;

}

h1, 

h2, 

h3, 

h4, 

h5, 

h6 {

	line-height: 1.25;

}

label {

	font-weight: 700;

}

.form-note {

	font-weight: 400;

	font-style: italic;

	color: #777;

}

.required {

	color: #f00;

}

.input-group-addon,

.form-control,

.custom-select,

.btn {

	line-height: 1.25;

	padding-top: 0.4375rem;

	padding-bottom: 0.4375rem;

	font-size: 0.875rem;

	-webkit-transition: all 200ms ease 0s;

	-moz-transition: all 200ms ease 0s;

	transition: all 200ms ease 0s;

}

.input-group-addon,

.form-control,

.custom-select {

	border-color: #dadada;

}

.form-control:focus,

.custom-select:focus {

	border-color: #732163;

}

.custom-select {

	padding-left: 0.5rem;

	padding-right: 1.75rem;

}

.btn {

	padding-left: 1.25rem;

	padding-right: 1.25rem;

}

.btn .icon {

	margin-right: 0.5rem;

}

.btn-secondary {

	color: #fff;

	background: #F22A70;

	border-color: #F22A70;

}

.btn-secondary:hover,

.btn-secondary:focus,

.btn-secondary:focus:active {

	color: #F22A70;

	background: #fff;

	border-color: #F22A70;

}

.btn-primary {

	color: #fff;

	background: #732163;

	border-color: #732163;

}

.btn-primary:hover,

.btn-primary:focus,

.btn-primary:focus:active {

	color: #732163;

	background: #fff;

	border-color: #732163;

}

.btn-outline-primary {

	color: #732163;

	background: #fff;

	border-color: #732163;

}

.btn-outline-primary:hover,

.btn-outline-primary:focus,

.btn-outline-primary:focus:active {

	color: #fff;

	background: #732163;

	border-color: #732163;

}

::-webkit-input-placeholder { 

	font-style: italic;

	color: #999;

}

::-moz-placeholder {

	font-style: italic;

	color: #999;

}

:-ms-input-placeholder { 

	font-style: italic;

	color: #999;

}

:-moz-placeholder { 

	font-style: italic;

	color: #999;

}



/*--------------------------------------------------------------

# Breadcrumb

--------------------------------------------------------------*/

.breadcrumb {

	padding: 1.25rem 0 1.25rem;

	margin: 0;

	background: transparent;

}

.breadcrumb-item:last-child a,

.breadcrumb-item a:hover,

.breadcrumb-item.active {

	color: #732163;

}

.breadcrumb-item + .breadcrumb-item:before {

	padding-left: 0.625rem;

	padding-right: 0.625rem;

	content: '\f105';

	font-family: FontAwesome;

	color: #888;

}



/*--------------------------------------------------------------

# Pagination

--------------------------------------------------------------*/

.nav-pagination {

	text-align: right;

	border-top: 1px solid #e5e5e5;

	padding-top: 0.9375rem;

	margin-top: 1.875rem;

}

.pagination {

	padding: 0;

	margin: 0;

}

.pagination .page-link {

	display: block;

	width: 2.25rem;

	height: 2.25rem;

	line-height: 2.125rem;

	padding: 0;

	margin-left: 0.625rem;

	margin-bottom: 0.625rem;

	text-align: center;

	color: #fff;

	background: #732163;

	border-color: #732163;

}

.pagination .page-link:hover,

.pagination .page-item.active .page-link {

	background: #F22A70;

	border-color: #F22A70;

}

.pagination .page-item:first-child .page-link,

.pagination .page-item:last-child .page-link {

	-webkit-border-radius: 0;

	-moz-border-radius: 0;

	border-radius: 0;

}



/*--------------------------------------------------------------

# Modal

--------------------------------------------------------------*/

.modal.fade-in-scale-up .modal-dialog {

	opacity: 0;

	-webkit-transform: scale(0.7);

	-moz-transform: scale(0.7);

	transform: scale(0.7);

	-webkit-transition: all 0.3s ease 0s;

	-moz-transition: all 0.3s ease 0s;

	transition: all 0.3s ease 0s;

}

.modal.fade-in-scale-up.in .modal-dialog {

	opacity: 1;

	-webkit-transform: scale(1);

	-moz-transform: scale(1);

	transform: scale(1);

}

.modal-content {

	border: 0;

	-webkit-box-shadow: 0 2px 12px rgba(0, 0, 0, 0.2);

	-moz-box-shadow: 0 2px 12px rgba(0, 0, 0, 0.2);

	box-shadow: 0 2px 12px rgba(0, 0, 0, 0.2);

}

.modal-header {

	padding: 15px 20px 10px;

	border-bottom: 0;

}

.modal-header .close {

	margin-top: 5px;

}

.modal-body {

	padding: 20px 20px;

}



/*--------------------------------------------------------------

# site header

--------------------------------------------------------------*/

/*--------------------------------------------------------------

## site top

--------------------------------------------------------------*/

.site-top {

	background: rgba(255,255,255,1);

	background: -moz-linear-gradient(top, rgba(255,255,255,1) 0%, rgba(246,246,246,1) 75%, rgba(237,237,237,1) 100%);

	background: -webkit-gradient(left top, left bottom, color-stop(0%, rgba(255,255,255,1)), color-stop(75%, rgba(246,246,246,1)), color-stop(100%, rgba(237,237,237,1)));

	background: -webkit-linear-gradient(top, rgba(255,255,255,1) 0%, rgba(246,246,246,1) 75%, rgba(237,237,237,1) 100%);

	background: -o-linear-gradient(top, rgba(255,255,255,1) 0%, rgba(246,246,246,1) 75%, rgba(237,237,237,1) 100%);

	background: -ms-linear-gradient(top, rgba(255,255,255,1) 0%, rgba(246,246,246,1) 75%, rgba(237,237,237,1) 100%);

	background: linear-gradient(to bottom, rgba(255,255,255,1) 0%, rgba(246,246,246,1) 75%, rgba(237,237,237,1) 100%);

	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ffffff', endColorstr='#ededed', GradientType=0 );

	padding: 0.625rem 0;

}

.site-schedule {

	float: left;

}

.site-schedule i {

	font-size: 1.25rem;

	color: #732163;

	margin-right: 0.3125rem;

}

.site-schedule strong {

	font-family: 'UTM Bebas';

	font-size: 1.25rem;

	font-weight: 400;

	text-transform: uppercase;

	color: #000;

	margin-right: 0.3125rem;

}

.site-search {

	float: right;

	width: 30rem;

}

.form-search .input-group-addon,

.form-search .form-control,

.form-search .btn {

	padding-top: 0.375rem;

	padding-bottom: 0.375rem;

}

.form-search .input-group-addon {

	background: #fff;

}

@media (max-width: 1199px) {

	.site-search {

		width: 22rem;

	}

}

@media (max-width: 991px) {

	.site-schedule {

		text-align: center;

		float: none;

	}

	.site-search {

		text-align: center;

		float: none;

		width: auto;

		margin-top: 0.3125rem;

	}

}



/*--------------------------------------------------------------

## site branding

--------------------------------------------------------------*/

.site-branding {

	padding: 1.25rem 0 1.25rem;

}

.site-logo {

	float: left;

	width: 50%;

	margin: 0;

}

.site-hotline {

	float: right;

	width: 50%;

        hight: auto;

}

@media (max-width: 991px) {

	.site-logo,

	.site-hotline {

		text-align: center;

		width: auto;

		float: none;

	}

	.site-hotline {

		margin-top: 2.925rem;

	}

}



/*--------------------------------------------------------------

## site navigation

--------------------------------------------------------------*/

.site-nav {

	background: #732163;

}

.site-nav ul {

	list-style: none;

	padding: 0;

	margin: 0;

	position: relative;

}

.site-nav ul:before,

.site-nav ul:after {

	content: ' ';

	display: block;

	clear: both;

}

.site-nav .menu > li {

	float: left;

}

.site-nav .menu > li + li {

	border-left: 1px solid #5AB0FF;

}

.site-nav .menu > li > a {

	display: block;

	line-height: 3rem;

	padding: 0 2rem;

	font-family: 'UTM Bebas';

	font-size: 1.25rem;

	font-weight: 400;

	text-transform: uppercase;

	color: #fff;

}

.site-nav .menu > li > a > i {

	font-size: 1.5rem;

}

.site-nav .menu > li:hover > a, 

.site-nav .menu > li:focus > a,

.site-nav .menu > li.current-menu-item > a,

.site-nav .menu > li.current-menu-parent > a {

	color: #fff;

	background: #F22A70;

}

.site-nav .menu > li > .sub-menu {

	background: #f0f0f0;

	box-shadow: 0 2px 3px rgba(0, 0, 0, 0.2);

	position: absolute;

	left: 0;

	top: 100%;

	width: 100%;

	z-index: 10;

	display: none;

	padding: 1.875rem 1.875rem;

}

.site-nav .menu > li:hover > .sub-menu {

	display: block;

}

.site-nav .menu-image {

	position: absolute;

	z-index: -1;

	top: 0; bottom: 0;

	left: 0; right: 0;

}

.site-nav .menu > li > .sub-menu > li {

	float: left;

	width: 25%;

	padding: 0 0.625rem;

}

.site-nav .menu > li > .sub-menu > li > a {

	font-weight: 700;

	text-transform: uppercase;

	color: #222;

	display: inline-block;

	margin-bottom: 0.3125rem;

}

.site-nav .sub-menu .sub-menu > li {

	margin-top: 0.3125rem;

}

.site-nav .sub-menu .sub-menu > li > a {

	-webkit-transition: all 200ms ease-in-out 0s;

	-moz-transition: all 200ms ease-in-out 0s;

	transition: all 200ms ease-in-out 0s;

}

.site-nav .sub-menu .sub-menu > li > a:hover {

	padding-left: 1.25rem;

}

.site-nav .sub-menu .sub-menu > li > a:before {

	content: '\f0fe';

	font-family: FontAwesome;

	font-size: 1.25rem;

	color: #732163;

	margin-right: 0.5rem;

}

@media (max-width: 1199px) {

	.site-nav .menu > li > a {

		padding: 0 1.25rem;

	}

}

@media (max-width: 991px) {

	.site-nav-toggler {

		padding: 0.25rem;

		font-size: 1.3125rem;

		color: #fff;

		background: transparent;

		border: 0;

	}

	.site-nav-toggler .text {

		margin-left: 0.5rem;

		font-size: 1.25rem;

		font-weight: 700;

	}

	.site-nav .menu > li {

		border-left: 1px solid #5AB0FF;

		float: none;

	}

	.site-nav .sub-menu {

		display: none !important;

	}

}



/*--------------------------------------------------------------

# site slider

--------------------------------------------------------------*/

.site-slider .item {

	display: block;

	padding-top: 38%;

	background-repeat: no-repeat;

	background-position: 50% 50%;

	background-size: cover;

}

.site-slider .owl-prev,

.site-slider .owl-next {

	position: absolute;

	top: 50%;

	margin-top: -3.75rem;

	font-size: 5rem;

	color: #fff;

}

.site-slider .owl-prev {

	left: 1.25rem;

}

.site-slider .owl-next {

	right: 1.25rem;

}



/*--------------------------------------------------------------

# category tabs

--------------------------------------------------------------*/

.cat-tabs .nav li {

	float: left;

	width: 20%;

}

.cat-tabs .nav li a {

	display: block;

	position: relative;

}

.cat-tabs .nav li a:before {

	content: ' ';

	display: block;

	position: absolute;

	z-index: 10;

	top: 0; left: 0;

	width: 100%;

	height: 100%;

	background: rgba(0, 0, 0, 0.4);

	-webkit-transition: all 0.3s ease 0s;

	-moz-transition: all 0.3s ease 0s;

	transition: all 0.3s ease 0s;

}

.cat-tabs .nav li a:hover:before,

.cat-tabs .nav li a.active:before {

	background: rgba(0, 0, 0, 0);

}

.cat-tabs .nav li img {

	width: 100%;

}

.cat-tabs .tab-pane {

	padding: 2.5rem 0;

}

.cat-tabs .tab-pane ul {

	list-style: none;

	padding: 0;

	margin: 0;

}

.cat-tabs .tab-pane ul li {

	position: relative;

	padding-left: 1.875rem;

	margin-bottom: 0.9375rem;

}

.cat-tabs .tab-pane ul li:before {

	content: '\f0fe';

	font-family: FontAwesome;

	font-size: 1.25rem;

	position: absolute;

	top: -0.25rem;

	left: 0;

	color: #732163;

}



/*--------------------------------------------------------------

# module

--------------------------------------------------------------*/

.module {

	padding: 3.125rem 0 0.625rem;

}

.module .module-title {

	font-family: 'UTM Bebas';

	font-size: 2.25rem;

	font-weight: 400;

	text-transform: uppercase;

	text-align: center;

	color: #732163;

	margin-bottom: 4.5rem;

}

.module .module-title .icon {

	background-color: transparent;

	background-position: center center;

	background-size: cover;

	display: inline-block;

	vertical-align: middle;

	width: 42px;

	height: 32px;

	margin-top: -0.3125rem;

	margin-right: 0.625rem;

}

.module .module-title .icon {

	background-image: url(images/icon-medkit.png);

}



/*--------------------------------------------------------------

# module reasons

--------------------------------------------------------------*/

.module-reasons {

	text-align: center;

	color: #fff;

	background: #732163;

}

.module-reasons .module-title {

	color: #fff;

}

.reason {

	margin-bottom: 2.5rem;

}

.reason figure {

	margin-bottom: 0;

}

.reason h3 {

	font-size: 1rem;

	font-weight: 700;

	margin-bottom: 0;

	margin-top: 1rem;

	text-align: center;

	text-transform: uppercase;

}

.reason p {

	margin-bottom: 0;

	margin-top: 1rem;

	text-align: justify;

}



/*--------------------------------------------------------------

# module consultant

--------------------------------------------------------------*/

.module-consultant .module-subtitle {

	    font-family: sans-serif;
    font-size: 17px;
    font-weight: bold;
    text-transform: uppercase;
    text-align: center;
    margin-bottom: 10px;
    margin-top: 15px;
    color: #732163;

}
.module-consultant .module-subtitle a{color: #732163}



/*--------------------------------------------------------------

# module banner

--------------------------------------------------------------*/

.module-banner img {

	width: 100%; 

}



/*--------------------------------------------------------------

# module knowledge

--------------------------------------------------------------*/

.module-knowledge-banner {

	text-align: center;

	margin-bottom: 2.5rem;

}



/*--------------------------------------------------------------

# module supports

--------------------------------------------------------------*/

.module-supports {

	background: #732163 ;

	padding-top: 1.875rem;

}

.support {

	margin-bottom: 1.25rem;

}

.support a {

	color: #fff;

}

.support .fa {

	font-size: 2.25rem;

	float: left;

	margin-right: 0.625rem;

}

.support p {

	line-height: 1.25;

	margin-bottom: 0;

}

.support .name-1 {

	font-size: inherit;

	font-weight: 700;

	text-transform: uppercase;

}



/*--------------------------------------------------------------

# module tess

--------------------------------------------------------------*/

.module-tess {

	padding-bottom: 3.125rem;

}

.tes {

	border: 0.125rem solid #732163;

	padding: 0.625rem;

}

.tes p {

	margin-top: 0.625rem;

	margin-bottom: 0;

}

.list-tess .owl-dots {

	text-align: center;

	margin-top: 0.625rem;

}

.list-tess .owl-dot {

	background: #ccc;

	display: inline-block;

	width: 0.625rem;

	height: 0.625rem;

	margin: 0 0.375rem;

}

.list-tess .owl-dot:hover,

.list-tess .owl-dot.active {

	 background: #732163;

}



/*--------------------------------------------------------------

# module slogan

--------------------------------------------------------------*/

.module-slogan {

	text-align: center;

}



/*--------------------------------------------------------------

# module environment

--------------------------------------------------------------*/

.module-env {

	padding-bottom: 3.125rem;

}

.env-gallery {

	background: #ccc;

	width: 960px;

	max-width: 100%;

	margin: 0 auto;

}

.env-gallery .dotsContainer {

	float: left;

	width: 25%;

	padding: 0.625rem 0.3125rem 0;

	margin: 0;

}

.env-gallery .dotsContainer .item {

	padding-left: 0.3125rem;

	padding-right: 0.3125rem;

	margin-bottom: 0.625rem;

}

.env-gallery .dotsContainer .item img {

	border: 1px solid transparent;

}

.env-gallery .dotsContainer .item:hover img,

.env-gallery .dotsContainer .item.active img {

	border-color: #732163;

}

.env-gallery .owl-carousel {

	float: left;

	width: 75%;

}

.env-gallery .owl-prev,

.env-gallery .owl-next {

	position: absolute;

	top: 50%;

	margin-top: -2.5rem;

	font-size: 3rem;

	color: #fff;

}

.env-gallery .owl-prev {

	left: 0.625rem;

}

.env-gallery .owl-next {

	right: 0.625rem;

}



/*--------------------------------------------------------------

# float news

--------------------------------------------------------------*/
.tom-tat a{background: #732163; border-radius:99px; padding: 3px 13px; color: white; display:inline-block}
.tom-tat{text-align:left !important; font-size:14px}
.list-float-news .hinh-anh1 img{
    transition: transform .2s;}
.list-float-news .hinh-anh1 img:hover {
    transform: scale(1.15);}

.list-float-news .hinh-anh1 {     margin-top: -30px;}
.list-float-news {text-align:center; display:inline-block;

	margin-bottom: 3.5rem;

}

.float-news:before,

.float-news:after {

	content: ' ';

	display: table;

	clear: both;

}

.float-news + .float-news {

	border-top: 1px solid #e5e5e5;

	padding-top: 0.9375rem;

	margin-top: 0.9375rem;

}

.float-news .image {

	position: relative;

	float: left;

	width: 35%;

	max-width: 7rem;

	margin-right: 0.625rem;

}

.news .image img {

	width: 100%;

}

.news .name,

.float-news .name {

	font-size: inherit;

	font-weight: 700;

	overflow: hidden;

	margin-bottom: 0.125rem;

}

.news .name a,

.float-news .name a {

	color: #555;

}

.news .name a:hover,

.float-news .name a:hover {

	color: #F22A70;

}

.news .name .excerpt,

.float-news .excerpt {

	margin-bottom: 0;

}



/*--------------------------------------------------------------

# news

--------------------------------------------------------------*/

.news {

	margin-bottom: 1.875rem;

}

.news .name {

	margin-top: 0.625rem;

	margin-bottom: 0.5rem;

}



/*--------------------------------------------------------------

# archive news

--------------------------------------------------------------*/

.archive-news .image {

	width: 30%;

	max-width: 12.5rem;

	margin-right: 0.9375rem;

}

.archive-news .name {

	font-size: 1.125rem;

	margin-bottom: 0.5rem;

}



/*--------------------------------------------------------------

# page

--------------------------------------------------------------*/

.page {

	-webkit-box-shadow: 0 0 0.5rem rgba(50, 50, 50, 0.1);

	-moz-box-shadow: 0 0 0.5rem rgba(50, 50, 50, 0.1);

	box-shadow: 0 0 0.5rem rgba(50, 50, 50, 0.1);

	padding: 0.9375rem;

	margin-bottom: 3.125rem;

}

.page-title {

	font-size: 1.5625rem;

	font-weight: 700;

	text-transform: uppercase;

	color: #732163;

	background: transparent url(images/icon-medkit.png) no-repeat left top 0.125rem;

	-webkit-background-size: 2.625rem auto;

	-moz-background-size: 2.625rem auto;

	background-size: 1.875rem auto;

	padding-left: 3rem;

	margin-bottom: 0.625rem;

}

.page-header {

	border-bottom: 1px solid #e5e5e5;

	padding-bottom: 1.875rem;

	margin-bottom: 0.9375rem;

}

.page-content {

	font-size: 0.9375rem;

	color: #222;

	margin-bottom: 2.5rem;

}

.page-content h2 {

	font-size: 18px;

	font-weight: 700;

	text-align: center !important;

	color: #fff;

	background: #732163 url(images/bg-h2.png) no-repeat;

	-webkit-background-size: cover;

	-moz-background-size: cover;

	background-size: cover;

	height: 35px;

	margin: 0rem 0 0.9375rem;

}

.page-content h2:before {

	content: ' ';

	display: inline-block;

	vertical-align: middle;

	width: 1px;

	height: 100%;

	margin-right: -4px;

}

.page-content h3 {

	font-size: 1rem;

	font-weight: 700;

	text-transform: uppercase;

	background: transparent url(http://mayo.com.vn/wp-content/themes/mayo-desktop/images/icon-posts/bg_title1.png) no-repeat left top;

	-webkit-background-size: 1.125rem auto;

	-moz-background-size: 1.125rem auto;

	background-size: 1.125rem auto;

	padding-left: 1.875rem;

	margin-bottom: 0.9375rem;

}

.page-content h4 {

	font-size: inherit;

	font-weight: 400;

	background: transparent url(images/icon-check-circle.png) no-repeat left top;

	-webkit-background-size: 1.125rem auto;

	-moz-background-size: 1.125rem auto;

	background-size: 1.125rem auto;

	padding-left: 1.875rem;

	margin-bottom: 0.9375rem;

}

.page-content p {

	margin-bottom: 1rem;

}

.page-content ul {

	list-style: none !important;

	padding-left: 1.875rem;

	margin-bottom: 1rem;

}

.page-content ul li {

	background: transparent url(images/icon-star.png) no-repeat left top 0.3125rem;

	-webkit-background-size: 0.75rem auto;

	-moz-background-size: 0.75rem auto;

	background-size: 0.75rem auto;

	padding-left: 1.5rem;

	margin-bottom: 0.3125rem;

}

.page-content ul[style*='disc'] li {

	background-image: url(images/icon-asterisk.png);

}

.page-content a {

	border-bottom: 1px solid #e5e5e5;

	color: #732163;

}

.page-content a:hover {

	color: #777;

	text-decoration: none;

}

.page-content table {

	border-collapse: collapse;

	border-spacing: 0;

	line-height: 2;

	margin-bottom: 2rem;

	width: 100%;

}

.page-content tbody {

	border-bottom: 1px solid #ddd;

}

.page-content th,

.page-content td {

	text-align: left;

}

.page-content th {

	font-weight: bold;

	text-transform: uppercase;

}

.page-content td {

	border-top: 1px solid #ddd;

	border-right: 1px solid #ddd;

	border-left: 1px solid #ddd;

	padding: 0.5rem;

}

.page-content img.centered,

.page-content .aligncenter {

	display: block;

	margin: 0 auto 1em;

}

.page-content img.alignnone {

	margin-bottom: 1em;

}

.page-content .alignleft {

	float: left;

	text-align: left;

}

.page-content .alignright {

	float: right;

	text-align: right;

}

.page-content img.alignleft,

.page-content .wp-caption.alignleft {

	margin: 0 1em 1em 0;

}

.page-content img.alignright,

.page-content .wp-caption.alignright {

	margin: 0 0 1em 1em;

}

.page-content .wp-caption {

	max-width: 100%;

}

.page-content .wp-caption img {

	width: 100%;

}

.page-content .wp-caption-text {

	margin-top: 0.5rem;

	font-weight: 400;

	font-style: italic;

	text-align: center;

}



img.hide {

	visibility: hidden;

}

.shock {

	display: inline-block;

	position: relative;

}

.shock-overlay {

	color: #fff;

	background: #666;

	border: 1px solid #ddd;

	text-align: center;

	position: absolute;

	z-index: 10;

	top: 0; 

	left: 0;

	width: 100%;

	height: 100%;

}

.shock-center {

	position: absolute;

	left: 50%;

	top: 50%;

	width: 90%;

	-webkit-transform: translate(-50%, -50%);

	-moz-transform: translate(-50%, -50%);

	transform: translate(-50%, -50%);

}

.shock-btn {

	color: #ee4a50 !important;

	background: #eee;

	border: 1px solid #ee4a50 !important;

}

.shock-btn:hover {

	color: #fff !important;

	background: #ee4a50;

}



.hotline {

	position: relative;

	margin-bottom: 1.25rem;

}

.hotline a img {

	position: absolute;

	z-index: 10;

	height: 3.75rem;

}

.hotline .image-1 {

	top: 0.625rem;

	right: 0.625rem;

}

.hotline .image-2 {

	top: 3.75rem;

	right: 0.625rem;

}

.hotline .image-3 {

	top: 7rem;

	right: 0.625rem;

}



/*--------------------------------------------------------------

# Post gallery

--------------------------------------------------------------*/

.gallery {

	margin-bottom: 1rem;

}

.gallery-item {

	margin-bottom: 0;

}

.gallery .owl-prev,

.gallery .owl-next {

	position: absolute;

	top: 50%;

	margin-top: -2.5rem;

	font-size: 3rem;

	color: #fff;

}

.gallery .owl-prev {

	left: 0.625rem;

}

.gallery .owl-next {

	right: 0.625rem;

}



/*--------------------------------------------------------------

# Form ask consultant

--------------------------------------------------------------*/

.form-ask-consultant {

	background: transparent url(images/bg-consultant.png) no-repeat center center;

	-webkit-background-size: cover;

	-moz-background-size: cover;

	background-size: cover;

	padding: 1.25rem 1.25rem 0.25rem;

	margin-bottom: 1.25rem;

}

.form-ask-consultant .form-control {

	background-color: #f2f2f2;

	background-repeat: no-repeat;

	background-position: left 0.3125rem bottom;

	-webkit-background-size: 2.25rem auto;

	-moz-background-size: 2.25rem auto;

	background-size: 2.25rem auto;

	border: 0.25rem solid #fff;

	padding-top: 0.625rem;

	padding-bottom: 0.625rem;

	padding-left: 3.125rem;

}

.form-ask-consultant .form-control[name='name'] {

	background-image: url(images/icon-user.png);

}

.form-ask-consultant .form-control[name='phone'] {

	background-image: url(images/icon-phone.png);

}

.form-ask-consultant .btn {

	font-size: 1rem;

	font-weight: 700;

	text-transform: uppercase;

	color: #fff;

	background: transparent url(images/bg-button.png) no-repeat center center;

	-webkit-background-size: cover;

	-moz-background-size: cover;

	background-size: cover;

	padding: 0.75rem 1.5rem;

	margin-top: 1.25rem;

}



/*--------------------------------------------------------------

# entry

--------------------------------------------------------------*/

.entry-title {

	font-family: 'UTM Bebas';

	font-size: 2rem; 

	font-weight: 400;

	text-transform: uppercase;

	color: #222;

	border-bottom: 1px solid #e5e5e5;

	padding-bottom: 0.625rem;

	margin-bottom: 0.9375rem;

}

.entry-excerpt {

	color: #222222;

	background: #F0FAF7;

	border: 1px solid #BDF0E2;

	line-height: inherit;

	font-size: inherit;

	font-weight: 400;

	font-style: italic;

	padding: 0.625rem 0.9375rem;

	margin-bottom: 1.25rem;

}

.entry-content {

	margin-bottom: 2.5rem;

	font-size: 0.9875rem;

	color: #222222;

}

.entry-content h1,

.entry-content h2,

.entry-content h3,

.entry-content h4,

.entry-content h5,

.entry-content h6 {

	font-family: 'UTM Bebas';

	font-size: 1.5rem;

	font-weight: 400;

	color: #fff;

	background: #732163;

	border-left: 0.3125rem solid #F22A70;

	text-align: center;

	position: relative;

	padding: 0.3125rem 0.625rem;

	margin-bottom: 1rem;

}

.entry-content a {

	border-bottom: 1px solid #e5e5e5;

	color: #732163;

}

.entry-content a:hover {

	color: #777;

	text-decoration: none;

}

.entry-content p {

	margin: 0 0 1em;

	padding: 0;

	text-rendering: geometricprecision;

}

.entry-content strong {

	font-weight: 700;

}

.entry-content ol {

	margin: 0 0 1.25rem 2.5rem;

	padding: 0;

}

.entry-content ol li {

	list-style-type: decimal;

}

.entry-content ol ol {

	margin-bottom: 0;

}

.entry-content ul {

	list-style: none !important;

	padding-left: 1.875rem;

	margin-bottom: 1rem;

}

.entry-content ul li {

	background: transparent url(images/icon-star.png) no-repeat left top 0.3125rem;

	-webkit-background-size: 0.75rem auto;

	-moz-background-size: 0.75rem auto;

	background-size: 0.75rem auto;

	padding-left: 1.5rem;

	margin-bottom: 0.3125rem;

}

.entry-content ul[style*='disc'] li {

	background-image: url(images/icon-asterisk.png);

}

.entry-content blockquote,

.entry-content blockquote::before {

}

.entry-content blockquote {

}

.entry-content blockquote::before {

}

.entry-content cite {

	font-style: normal;

}

.entry-content h1,

.entry-content h2,

.entry-content h3,

.entry-content h4,

.entry-content h5,

.entry-content h6 {

	font-weight: 400;

	margin-bottom: 0.75rem;

}

.entry-content table {

	border-collapse: collapse;

	border-spacing: 0;

	line-height: 2;

	margin-bottom: 2rem;

	width: 100%;

}

.entry-content tbody {

	border-bottom: 1px solid #ddd;

}

.entry-content th,

.entry-content td {

	text-align: left;

}

.entry-content th {

	font-weight: bold;

	text-transform: uppercase;

}

.entry-content td {

	border-top: 1px solid #ddd;

	padding: 0.5rem;

}

.entry-content img.centered,

.entry-content .aligncenter {

	display: block;

	margin: 0 auto 1em;

}

.entry-content img.alignnone {

	margin-bottom: 1em;

}

.entry-content .alignleft {

	float: left;

	text-align: left;

}

.entry-content .alignright {

	float: right;

	text-align: right;

}

.entry-content img.alignleft,

.entry-content .wp-caption.alignleft {

	margin: 0 1em 1em 0;

}

.entry-content img.alignright,

.entry-content .wp-caption.alignright {

	margin: 0 0 1em 1em;

}

.entry-content .wp-caption {

	max-width: 100%;

}

.entry-content .wp-caption img {

	width: 100%;

}

.entry-content .wp-caption-text {

	margin-top: 0.5rem;

	font-weight: 400;

	font-style: italic;

	text-align: center;

}



.entry-tags {

	padding-top: 1rem;

	margin-bottom: 1.25rem;

	border-top: 1px dotted #aaa;

}

.entry-tags .title {

	float: left;

	margin-right: 0.75rem;

	margin-bottom: 0.625rem;

	font-size: 0.9375rem; font-weight: bold;

	color: #222;

}

.entry-tags ul {

	list-style: none;

	padding: 0;

	margin: 0;

}

.entry-tags li {

	float: left;

	margin-right: 0.75rem;

	margin-bottom: 0.75rem;

}

.entry-tags a {

	display: block;

	padding: 0.125rem 0.75rem;

	font-size: 0.9375rem;

	color: #fff;

	background: #555;

	-webkit-border-radius: 0.25rem;

	-moz-border-radius: 0.25rem;

	border-radius: 0.25rem;

}

.entry-tags a:hover,

.entry-tags a:focus {

	color: #fff;

	background: #F22A70;

	border-color: #F22A70;

}



.entry-comments {

	border-top: 1px solid #ddd;

	padding-top: 0.9375rem;

	margin-bottom: 1.875rem;

}

.entry-comments .title {

	margin-bottom: 0.9375rem;

	font-size: 1.25rem; font-weight: bold;

	text-transform: uppercase;

	color: #732163;

}

.comments {

	list-style: none;

	padding: 0;

	margin-bottom: 1.875rem;

}

.child-comments {

	margin-left: 2rem;

	margin-bottom: 0;

}

.comment,

.child-comments {

	font-size: 0.8125rem;

	padding-top: 0.625rem;

	margin-top: 0.625rem;

	border-top: 1px dotted #aaa;

}

.comment:first-child {

	border-top: 0;

	padding-top: 0;

	margin-top: 0;

}

.comment .content {

	clear: both;

	margin-top: 0.3125rem;

	margin-bottom: 0;

}

.comment .avatar {

	margin-right: 0.25rem;

}

.comment .name {

	font-weight: 700;

	color: #555;

}

.comment .time {

	color: #999;

}

.comment .reply {

	font-size: 0.8125rem;

	float: right;

}

.comment .reply .icon {

	margin-right: 0.25rem;

}



/*--------------------------------------------------------------

# module related posts

--------------------------------------------------------------*/

.module-related-posts {

	margin-bottom: 2.5rem;

}

.module-related-posts .module-title {

	font-family: 'UTM Bebas';

	font-size: 1.75rem;

	text-transform: uppercase;

	color: #732163;

	border-bottom: 1px solid #e5e5e5;

	margin-bottom: 0.9375rem;

}

.module-related-posts .module-title strong {

	font-weight: 400;

	border-bottom: 1px solid #732163;

	display: inline-block;

	padding-bottom: 0.3125rem;

}

.list-news {

	list-style: none;

	padding: 0;

	margin: 0;

}

.list-news li {

	margin-bottom: 0.625rem;

}

.list-news li a {

	font-size: 1rem;

	color: #222;

}

.list-news li a:hover {

	color: #732163;

}

.list-news li a:before {

	content: '\f105';

	font-family: FontAwesome;

	margin-right: 0.5rem;

}



/*--------------------------------------------------------------

# widget

--------------------------------------------------------------*/

.widget {

	overflow: hidden;

	-webkit-border-radius: 0.25rem;

	-moz-border-radius: 0.25rem;

	border-radius: 0.25rem;

	-webkit-box-shadow: 0 0.25rem 0.3125rem rgba(50, 50, 50, 0.1);

	-moz-box-shadow: 0 0.25rem 0.3125rem rgba(50, 50, 50, 0.1);

	box-shadow: 0 0.25rem 0.3125rem rgba(50, 50, 50, 0.1);

	margin-bottom: 1.875rem;

}

.widget_text {

	text-align: center;

	-webkit-border-radius: 0;

	-moz-border-radius: 0;

	border-radius: 0;

	-webkit-box-shadow: none;

	-moz-box-shadow: none;

	box-shadow: none;

}

.widget .widget-title {

	font-family: 'UTM Bebas';

	font-size: 1.25rem;

	font-weight: 400;

	color: #fff;

	background: #732163;

	padding: 0.5rem 0.9375rem;

	margin-bottom: 0;

}

.widget > div {

	padding: 0.9375rem;

}

.widget > .textwidget {

	padding: 0;

}

.widget ul {

	list-style: none;

	padding: 0;

	margin: 0;

}

.widget ul li + li {

	margin-top: 0.625rem;

}

.widget ul li a {

	font-weight: 700;

}

.widget_support .widget-content {

	background-repeat: no-repeat;

	background-position: right bottom;

}

.widget_support table th {

	font-size: 1rem;

	font-weight: 400;

	text-transform: uppercase;

	color: #f00;

	padding-right: 0.3125rem;

}

.widget_support table td {

	font-size: 1rem;

	text-transform: uppercase;

}

.widget_support p {

	font-weight: 700;

	text-transform: uppercase;

	color: #f00;

	margin-top: 0.3125rem;

}

.widget_support a {

	display: block;

	width: 10rem;

	margin: 0 auto;

}



/*--------------------------------------------------------------

# footer

--------------------------------------------------------------*/

/*--------------------------------------------------------------

# footer navigations

--------------------------------------------------------------*/

.footer-navs {

	background: transparent url(images/footer-bg.png) no-repeat center bottom;

	position: relative;

	padding: 3.75rem 0 5rem;

}

.footer-navs:before {

	content: ' ';

	display: block;

	position: absolute;

	z-index: -1;

	top: 0; bottom: 0;

	left: 0; right: 0;

	background: rgba(206,234,246,1);

	background: -moz-linear-gradient(top, rgba(206,234,246,1) 0%, rgba(255,255,255,1) 60%, rgba(255,255,255,1) 100%);

	background: -webkit-gradient(left top, left bottom, color-stop(0%, rgba(206,234,246,1)), color-stop(60%, rgba(255,255,255,1)), color-stop(100%, rgba(255,255,255,1)));

	background: -webkit-linear-gradient(top, rgba(206,234,246,1) 0%, rgba(255,255,255,1) 60%, rgba(255,255,255,1) 100%);

	background: -o-linear-gradient(top, rgba(206,234,246,1) 0%, rgba(255,255,255,1) 60%, rgba(255,255,255,1) 100%);

	background: -ms-linear-gradient(top, rgba(206,234,246,1) 0%, rgba(255,255,255,1) 60%, rgba(255,255,255,1) 100%);

	background: linear-gradient(to bottom, rgba(206,234,246,1) 0%, rgba(255,255,255,1) 60%, rgba(255,255,255,1) 100%);

	filter: progid:DXImageTransform.Microsoft.gradient( startColorstr='#ceeaf6', endColorstr='#ffffff', GradientType=0 );

}

.footer-navs .row {

	margin-left: -0.625rem;

	margin-right: -0.625rem;

}

.footer-nav {

	display: inline-block;

	vertical-align: top;

	width: 20%;

	padding: 0 0.625rem;

	margin-right: -4px;

	margin-bottom: 1.875rem;

}

.footer-nav .widget-title {

	font-size: 1rem;

	font-weight: 700;

	text-transform: uppercase;

	color: #732163;

	border: 0.1875rem dotted #2B7FC4;

	border-right: 0;

	border-radius: 0.375rem 0 0 0.375rem;

	display: inline-block;

	padding: 0.375rem 0 0.25rem 0.625rem;

	margin-bottom: 1.25rem;

}

.footer-nav ul {

	list-style: none;

	padding: 0;

	margin: 0;

}

.footer-nav ul li + li {

	margin-top: 0.5rem;

}

.footer-nav ul li a {

	color: #732163;

	display: inline-block;

	position: relative;

	padding-left: 1.5rem;

}

.footer-nav ul li a:hover {

	color: #F22A70;

}

.footer-nav li a:before {

	content: '\f069';

	font-family: FontAwesome;

	position: absolute;

	top: 0;

	left: 0;

}

.footer-note {

	text-align: center;

	font-style: italic;

}

@media (max-width: 1199px) {

	.footer-nav {

		width: 33.3333%;

	}

}

@media (max-width: 543px) {

	.footer-nav {

		width: 100%;

	}

}



/*--------------------------------------------------------------

# footer main

--------------------------------------------------------------*/

.footer-main {

	padding: 1.875rem 0 1.25rem;

}

.footer-logo {

	text-align: center;

	margin-bottom: 1.25rem;

}

.footer-desc {

	text-align: center;

}

.footer-social {

	text-align: center;

	list-style: none;

	padding: 0;

	margin: 0;

}

.footer-social li {

	display: inline-block;

	margin: 0 0.3125rem 0.3125rem;

}

.footer-social li a {

	font-size: 3rem;

}

.footer-social li.facebook a {

	color: #3664A2;

}

.footer-social li.google-plus a {

	color: #FF3334;

}

.footer-social li.youtube a {

	color: #D23337;

}

.footer-map {

	padding-top: 72%;

	margin-bottom: 1.25rem;

}

.footer-copyright {

	font-weight: 700;

	text-align: center;

	color: #fff;

	background: #732163;

	padding-bottom: 1.25rem;

}



/*--------------------------------------------------------------

# Banner

--------------------------------------------------------------*/

.banner-left {

	position: fixed;

	z-index: 999;

	left: 0;

	top: 8rem;

	text-align: right;

	visibility: visible;

}

.banner-left .close {

	font-size: 0.5625rem;

	font-weight: 700;

	color: #e20e0e;

	background-color: rgba(0, 0, 0, 0.05);

	-webkit-border-radius: 50%;

	-moz-border-radius: 50%;

	border-radius: 50%;

	text-align: center;

	position: absolute;

	left: 0;

	top: -0.125rem;

	width: 1.25rem;

	height: 1.25rem;

	line-height: 1.25rem;

	opacity: 1;

}

.banner-left .close:hover {

	background-color: rgba(0, 0, 0, 0.1);

}



/*--------------------------------------------------------------

# Toolbar

--------------------------------------------------------------*/

.toolbar {

	background-color: rgba(0, 0, 0, 0.5);

	border-top: 1px solid #fff;

	color: #fff;

	cursor: pointer;

	position: fixed;

	z-index: 1000;

	left: 0;

	bottom: 0;

	width: 100%;

}

.toolbar .col {

	padding-top: 0.625rem;

	padding-bottom: 0.625rem;

}

.toolbar .col + .col {

	border-left: 1px solid #fff;

}

.toolbar p {

	margin-bottom: 0;

}

.toolbar a {

	color: #fff;

}

.toolbar img {

	bottom: 0;

	position: absolute;

	right: 1.25rem;

	width: 42%;

}

.form-get-phone {

	margin-top: 0.5rem;

	margin-bottom: 0.5rem;

}

.form-get-phone .form-control,

.form-get-phone .btn {

	padding: 0.3125rem 0.625rem;

}

.toolbar ul {

	list-style: none;

	padding: 0;

	margin: 0;

}

.toolbar ul li {

	display: inline-block;

	vertical-align: top;

	margin-right: 1.25rem;

}
.site-logo img {
	width: 250px;
}
.tt-video{
	padding-top: 50px;
}
.tt-video .module-title{
	font-family: 'UTM Bebas';
    font-size: 2.25rem;
    font-weight: 400;
    text-transform: uppercase;
    text-align: center;
    color: #732163;
    margin-bottom: 4.5rem;
}
