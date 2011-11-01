#Webfonts Bundle

Selection of free Webfonts. Wrapped in Symfony2 Bundle
most of them generated using http://www.fontsquirrel.com/fontface/generator

##Installation

###1. update deps file
Add the following lines to your deps file

	[JirgnAssetsWebfontsBundle]
		git=https://github.com/jirgn/JirgnAssetsWebfontsBundle.git
		target=/bundles/Jirgn/Assets/WebfontsBundle

###2. trigger vendor update
use bin/vendors update command to get the repository

###3. register namespaces
add following code to your app/autoload.php

	$loader->registerNamespaces(array(
		...
		'Jirgn'=> __DIR__.'/../vendor/bundles',
		...
	);
###4. add bundle to kernel
add following code to your app/AppKernel.php::

	public function registerBundles()
		{
		...
		new Jirgn\Assets\WebfontsBundle\JirgnAssetsWebfontsBundle(),
	}
