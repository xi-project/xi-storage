# Simple file storage

Create a storage object for arbitrary, persistent data, then manipulate 
it later. Each object has exactly one backend determined by the 
implementation, eg. a filesystem file or session variable. Modelled 
after Zend_Auth_Storage.

Usage:

	$file = new \Xi\Storage\FileStorage(__DIR__ . '/example.txt');
	$file->write('foo');
	echo $file->read();
	$file->clear();