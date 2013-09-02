# CodeIgniter-Imagick-Library

CodeIgniter-Imagick is a CodeIgniter library which makes it easy to create simple image with font and do some image edit easier too.

# Requirement

1. PHP 5.1+
2. Codeigniter 2.1.4
3. PHP >= 5.1.3 
4. ImageMagick >= 6.2.4 

# Usage
	public function index()
	{
		$config = array('font'=>'yahei',
						'font_path'=>'font/',
						'color'=>'#333333',
						'size'=>25,
						'font_image_width'=>700,
						'font_image_height'=>1000,
						'font_border_size'=>30,
						'word_distence'=>5,
						'word_line_distance'=>10,
						'image_format'=>'png',
						'string'=>'UFO全称为不明飞行物，也称飞碟（unidentified flying object，简称UFO）是指不明来历、不明空间、不明结构、不明性质，但又漂浮、飞行在空中的物体。一些人相信它是来自其他行星的太空船，有些人则认为UFO属于自然现象。20世纪40年代开始，美国上空发现碟状飞行物，当时称为飞碟，这是当代对不明飞行物的兴趣的开端，后来人们着眼于世界各地的不明飞行物报告，但至今尚未发现确实可信的证据。许多不明飞行物照片经专家鉴定为骗局，有的则被认为是球状闪电，但始终有部分发现根据现存科学知识无法解释。',
						'out_put_path'=>'/',
						'file_name'=>'test');

		$this->load->library('imagick_lib',$config);
		$this->imagick_lib->create_background();
		$this->imagick_lib->render();
	}
	
Image will be output to /test.png 