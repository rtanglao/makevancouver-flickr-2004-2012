# makevancouver-flickr-2004-2012
code to make tshirts for makevancouver from flickr-2004-2012

## December 25, 2016

* copy https://github.com/rtanglao/2016-rtgram/blob/master/create5x5thumbnails.rb to this directory
* ```mkdir 5x5```
*  run it on flickr 2004-2012:

```sh
 ./create5x5thumbnails.rb /Users/rtanglao/Dropbox/Public/CCC/DATASETS/09April2012-ROLAND-103K-75x75-FLICKR-PHOTOS/75X75/FILES_SYM_LINKED_SEQUENTIALLY 5x5/
```
* ```mkdir 10x10```
* try 10x10 thumbnails because that fits better: 
```sh
./create10x10thumbnails.rb /Users/rtanglao/Dropbox/Public/CCC/DATASETS/09April2012-ROLAND-103K-75x75-FLICKR-PHOTOS/75X75/FILES_SYM_LINKED_SEQUENTIALLY 10x10/
```
* 3200x2400 target png: 320*240=76800 thumbanils
* ```cd 10x10; ls -1 | head -76800 >1st76800pngs.txt```
* ```gm montage -verbose -adjoin -tile 320x240 +frame +shadow +label -adjoin -geometry '10x10+0+0<' @1st76800pngs.txt montage320x240-flickr-2004-2012-1st76800-10x10.png```
