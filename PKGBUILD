# SPDX-License-Identifier: AGPL-3.0

#    ----------------------------------------------------------------------
#    Copyright © 2024, 2025  Pellegrino Prevete
#
#    All rights reserved
#    ----------------------------------------------------------------------
#
#    This program is free software: you can redistribute it and/or modify
#    it under the terms of the GNU Affero General Public License as published by
#    the Free Software Foundation, either version 3 of the License, or
#    (at your option) any later version.
#
#    This program is distributed in the hope that it will be useful,
#    but WITHOUT ANY WARRANTY; without even the implied warranty of
#    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
#    GNU Affero General Public License for more details.
#
#    You should have received a copy of the GNU Affero General Public License
#    along with this program.  If not, see <https://www.gnu.org/licenses/>.

# Maintainer:
#   Truocolo
#     <truocolo@aol.com>
#     <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
# Maintainer:
#   Pellegrino Prevete (dvorak)
#     <pellegrinoprevete@gmail.com>
#     <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>

_evmfs_available="$( \
  command \
    -v \
    "evmfs" || \
    true)"
if [[ ! -v "_evmfs" ]]; then
  if [[ "${_evmfs_available}" != "" ]]; then
    _evmfs="true"
  elif [[ "${_evmfs_available}" == "" ]]; then
    _evmfs="false"
  fi
fi
if [[ ! -v "_docs" ]]; then
  _docs="true"
fi
if [[ ! -v "_git" ]]; then
  _git="false"
fi
if [[ ! -v "_offline" ]]; then
  _offline="false"
fi
_os="$( \
  uname \
    -o)"
_py="python"
_pkg=videogame-launcher
pkgbase="${_pkg}"
pkgname=(
  "${pkgbase}"
)
if [[ "${_docs}" == "true" ]]; then
  pkgname+=(
    "${pkgbase}-docs"
  )
fi
pkgver="0.0.0.0.0.0.0.0.0.0.0.1.1.1.1.1.1.1.1.1"
_commit="4ed5c6e6f4ec299bd26d15d45edcd829c039fa83"
pkgrel=1
_pkgdesc=(
  "Seamlessly launch videogames"
  "with multiple backend."
)
pkgdesc="${_pkgdesc[*]}"
arch=(
  'any'
)
_http="https://github.com"
_ns="themartiancompany"
url="${_http}/${_ns}/${pkgname}"
license=(
  'AGPL3'
)
depends=(
  "libcrash-bash"
)
makedepends=(
  'make'
)
if [[ "${_docs}" == "true" ]]; then
  makedepends+=(
    "${_py}-docutils"
  )
fi
checkdepends=(
  "shellcheck"
)
_duckstation_optdepends=(
  "duckstation:"
    "launch PlayStation videogames"
    "with Duckstation."
)
_fceux_optdepends=(
  "fceux:"
    "launch Nintendo Entertainment"
    "System videogames with FCEUX."
)
_gearboy_optdepends=(
  "gearboy:"
    "launch GameBoy videogames"
    "with Gearboy."
)
_pcsx2_16_optdepends=(
  "pcsx2-1.6:"
    "launch PlayStation 2"
    "videogames with PCSX2>=1.6.x"
    "(>=SSE2 CPUs)."
)
_pcsx2_17_optdepends=(
  "pcsx2-1.7:"
    "launch PlayStation 2"
    "videogames with PCSX2>=1.7.x"
    "(>=SSE3 CPUs)."
)
_pcsx2_optdepends=(
  "pcsx2:"
    "launch PlayStation 2"
    "videogames with PCSX2"
    "(>=SSE4 CPUs)."
)
_retroarch_optdepends=(
  "retroarch:"
    "launch videogames"
    "with RetroArch."
)
_retroarch_nintendo64_optdepends=(
  "libretro-mupen64plus-next:"
    "launch Nintendo 64"
    "videogames"
    "with RetroArch."
)
_retroarch_scummvm_optdepends=(
  "libretro-scummvm:"
    "launch SCUMMVM"
    "videogames"
    "with RetroArch."
)
_scummvm_optdepends=(
  "scummvm:"
    "launch SCUMMVM"
    "videogames."
)
optdepends+=(
  "${_duckstation_optdepends[*]}"
  "${_fceux_optdepends[*]}"
  "${_gearboy_optdepends[*]}"
  "${_pcsx2_16_optdepends[*]}"
  "${_pcsx2_17_optdepends[*]}"
  "${_pcsx2_optdepends[*]}"
  "${_retroarch_optdepends[*]}"
  "${_retroarch_nintendo64_optdepends[*]}"
  "${_scummvm_optdepends[*]}"
)
source=()
sha256sums=()
_url="${url}"
_tag="${_commit}"
_tag_name="commit"
_tarname="${_pkg}-${_tag}"
if [[ "${_offline}" == "true" ]]; then
  _url="file://${HOME}/${_pkg}"
  _tarname="${_pkg}"
fi
_evmfs_network="100"
_evmfs_address="0x69470b18f8b8b5f92b48f6199dcb147b4be96571"
_evmfs_ns="0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b"
_archive_sum="c3afa76d447384917b028c0c8d75081a2f7febbb9c694691c85e51864e83f8bc"
_evmfs_archive_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_archive_sum}"
_evmfs_archive_src="${_tarname}.tar.xz::${_evmfs_archive_uri}"
_archive_sig_sum="cde6e4aace6a1e0cc6cd8fb899209456379a3c1ae6f938703a3729d16e5f7e36"
_archive_sig_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_archive_sig_sum}"
_archive_sig_src="${_tarname}.tar.xz.sig::${_archive_sig_uri}"
if [[ "${_evmfs}" == true ]]; then
  makedepends+=(
    "evmfs"
  )
  _src="${_evmfs_archive_src}"
  _sum="${_archive_sum}"
  source+=(
    "${_archive_sig_src}"
  )
  sha256sums+=(
    "${_archive_sig_sum}"
  )
elif [[ "${_git}" == true ]]; then
  makedepends+=(
    "git"
  )
  _src="${_tarname}::git+${_url}#${_tag_name}=${_tag}?signed"
  _sum="SKIP"
elif [[ "${_git}" == false ]]; then
  if [[ "${_tag_name}" == 'pkgver' ]]; then
    _src="${_tarname}.tar.gz::${_url}/archive/refs/tags/${_tag}.tar.gz"
    _sum="d4f4179c6e4ce1702c5fe6af132669e8ec4d0378428f69518f2926b969663a91"
    _sum="Who cares, fetching stuff using tags with git is unsecure."
  elif [[ "${_tag_name}" == "commit" ]]; then
    _src="${_tarname}.zip::${_url}/archive/${_commit}.zip"
    _sum="${_archive_sum}"
  fi
fi
source+=(
  "${_src}"
)
sha256sums+=(
  "${_sum}"
)

validpgpkeys=(
  # Truocolo <truocolo@aol.com>
  '97E989E6CF1D2C7F7A41FF9F95684DBE23D6A3E9'
  'DD6732B02E6C88E9E27E2E0D5FC6652B9D9A6C01'
  # Truocolo (kf) <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
  'F690CBC17BD1F53557290AF51FC17D540D0ADEED'
)

check() {
  cd \
    "${_tarname}"
  make \
    -k \
    check
}

package_videogame-launcher() {
  local \
    _make_opts=()
  depends+=(
    "libcrash-bash"
  )
  _make_opts=(
    DESTDIR="${pkgdir}"
    PREFIX='/usr'
  )
  cd \
    "${_tarname}"
  make \
    "${_make_opts[@]}" \
    install-configs
  make \
    "${_make_opts[@]}" \
    install-scripts
  install \
    -vDm644 \
    "COPYING" \
    "${pkgdir}/usr/share/licenses/${pkgname}"
}

package_videogame-launcher-docs() {
  local \
    _make_opts=()
  _make_opts=(
    DESTDIR="${pkgdir}"
    PREFIX='/usr'
  )
  cd \
    "${_tarname}"
  make \
    "${_make_opts[@]}" \
    install-doc
  make \
    "${_make_opts[@]}" \
    install-man
}

# vim:set sw=2 sts=-1 et:
