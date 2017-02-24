# Maintainer: Corey Hinshaw <coreyhinshaw@gmail.com>
# Contributor: Max Resch <resch.max@gmail.com>

pkgname=mkinitcpio-tpm-hook
pkgver=0.1.0
pkgrel=1
pkgdesc="Decrypt your root filesystem with a TPM-sealed keyfile"
arch=('any')
url="https://github.com/electrickite/mkinitcpio-tpm-hook"
license=('GPL')
depends=('mkinitcpio' 'tpm-tools' 'trousers' 'glibc' 'gcc-libs')
source=('install_tpm'
        'hook_tpm'
        'hosts'
        'passwd'
        'README.md')

sha256sums=('c4049a43b9616faa091a95386c1342562c21b832a6aa8a275db320022e20d939'
            '4b05b7bdc413238dae5e3790299575db17f37850176265afc2305b8d3db57c72'
            'b30167ccb1927f0f62dfb658fee49ba857b3f7b85cc6a4d3c659236bb01b1a03'
            '4b263523f4904bfe340a3208f327697ebd78f9f921e8be0dabdf33535c54a1b5'
            'e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855')

package() {
  install -Dm644 install_tpm "${pkgdir}/usr/lib/initcpio/install/tpm"
  install -Dm644 hook_tpm "${pkgdir}/usr/lib/initcpio/hooks/tpm"
  install -Dm644 hosts "${pkgdir}/usr/lib/initcpio/tpm/hosts"
  install -Dm644 passwd "${pkgdir}/usr/lib/initcpio/tpm/passwd"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README"
}
