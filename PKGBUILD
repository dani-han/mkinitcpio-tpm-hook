# Maintainer: Corey Hinshaw <coreyhinshaw@gmail.com>
# Contributor: Max Resch <resch.max@gmail.com>

pkgname=mkinitcpio-tpm-hook
pkgver=0.1.2
pkgrel=1
pkgdesc="Decrypt your root filesystem with a TPM-sealed keyfile"
arch=('any')
url="https://github.com/electrickite/mkinitcpio-tpm-hook"
license=('GPL')
depends=('mkinitcpio' 'tpm-tools' 'trousers')
source=('install_tpm'
        'hook_tpm'
        'hosts'
        'passwd'
        'README.md')

sha256sums=('96ca20898dd38c4828da7e9dede1d09bd752a4f8961420f0a064e74cf9a4b711'
            'f3838a94134498cd5544932df606836dac599d7923d2b7f0ca0615b99d5981a7'
            'b30167ccb1927f0f62dfb658fee49ba857b3f7b85cc6a4d3c659236bb01b1a03'
            '4b263523f4904bfe340a3208f327697ebd78f9f921e8be0dabdf33535c54a1b5'
            'c3e777c9d620927045991a88723b06d2947ced566ce6404239662006b9e186c6')

package() {
  install -Dm644 install_tpm "${pkgdir}/usr/lib/initcpio/install/tpm"
  install -Dm644 hook_tpm "${pkgdir}/usr/lib/initcpio/hooks/tpm"
  install -Dm644 hosts "${pkgdir}/usr/lib/initcpio/tpm/hosts"
  install -Dm644 passwd "${pkgdir}/usr/lib/initcpio/tpm/passwd"
  install -Dm644 README.md "${pkgdir}/usr/share/doc/${pkgname}/README"
}
