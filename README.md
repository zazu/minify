# Kohana 3.0 Minify Module 

Simple Minify wrapper for Kohana 3. Yet basically tailored to suit my needs in a specific project.

## Usage

    // Minify given string / file contents
    $min = Minify::factory('js')->set( $filecontents )->min();
    $min = Minify::factory('css')->set( $filecontents )->min(); 

    // Minify list of files; 
	//write result into media folder as defined in config
	// use md5 hash of filelist and apps build number as filename
	
    Controller::after()  
    $this->template->jsFiles = Minify::factory('js')->minify( $this->template->jsFiles, $build );
    $this->template->cssFiles = Minify::factory('css')->minify( $this->template->cssFiles, $build );


## Credits

BASED ON THE JSMIN CODE BY rgrove: http://code.google.com/p/jsmin-php 

BASED ON THE CSSMIN CODE BY joe.scylla: http://code.google.com/p/cssmin

BASED ON THE Kohana 2 Minify Driver by Tom Morton 
