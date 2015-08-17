# Maintainer: Alessandro Pezzoni <alessandro_pezzoni@lavabit.com>
# Contributor: <ndowens.aur at gmail dot com>
pkgname=vim-cctree
pkgver=1.61
pkgrel=2
pkgdesc="C Call-Tree Explorer - Source-code analysis, real-time display of code flow"
arch=("any")
url="http://www.vim.org/scripts/script.php?script_id=2368"
license=('custom')
depends=("vim" "cscope")
optdepends=('ccglue: Generate cross-reference cctree database files')
install=vimdoc.install
source=("cctree.vim::http://www.vim.org/scripts/download_script.php?src_id=18112"
        "cctree.txt::https://sites.google.com/site/vimcctree/cctree.txt?attredirects=0"
        "LICENSE")
md5sums=('14bac0bd4e75eb7a99ab4fef4318bd88'
         '6e7dd920acdcf3eb636098434a3cbeb2'
         '524189b81e0caaf10e6469a01c3b3db9')

package() {
	  cd $srcdir/ 

	  install -d ${pkgdir}/usr/share/{licenses/$pkgname,vim/vimfiles/{doc,plugin}}
	  
	  install -Dm644 cctree.vim \
	  	  ${pkgdir}/usr/share/vim/vimfiles/plugin/cctree.vim
          
          install -Dm644 cctree.txt \
	  	  ${pkgdir}/usr/share/vim/vimfiles/doc/CCTree.txt
	  
	  install -Dm644 $srcdir/LICENSE \
	  	  $pkgdir/usr/share/licenses/$pkgname
}
