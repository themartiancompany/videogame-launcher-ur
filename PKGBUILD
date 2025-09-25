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
if [[ ! -v "_mirror_type" ]]; then
  _mirror_type="public"
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
pkgver="0.0.0.0.0.0.0.0.0.0.1.1.1.1"
_commit="ded8f868f8fba6d54d6c7454a6e98833e9f9b08c"
pkgrel=1
_pkgdesc=(
  "Seamlessly launch videogames"
  "with multiple backend."
)
pkgdesc="${_pkgdesc[*]}"
arch=(
  'any'
)
if [[ "${_mirror_type}" == "public" ]]; then
  _http="https://github.com"
elif [[ "${_mirror_type}" == "private" ]]; then
  _http="https://gitlab.com"
fi
_ns="themartiancompany"
url="${_http}/${_ns}/${pkgname}"
license=(
  'AGPL3'
)
depends=(
  "coreutils"
  "libcrash-bash"
  "sed"
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
_doomretro_optdepends=(
  "doomretro:"
    "Support for launching"
    "Doom and Doom-engine"
    "based videogames."
)
_dosbox_optdepends=(
  "dosbox:"
    "Support for launching"
    "DOS videogames."
)
_duckstation_optdepends=(
  "duckstation:"
    "Support for launching"
    "PlayStation videogames"
    "with Duckstation."
)
_fceux_optdepends=(
  "fceux:"
    "Support for launching Nintendo"
    "Entertainment System videogames"
    "with FCEUX."
)
_famicom_bios_optdepends=(
  "famicom-bios:"
    "Support for launching Nintendo"
    "FamiCom videogames"
    "with FCEUX."
)
_flycast_optdepends=(
  "flycast:"
    "Support for launching Sega"
    "Dreamcast videogames"
    "with Flycast."
)
_gearboy_optdepends=(
  "gearboy:"
    "Support for launching GameBoy"
    "videogames with Gearboy."
)
_pcsx2_16_optdepends=(
  "pcsx2-1.6:"
    "Support for launching PlayStation 2"
    "videogames with PCSX2>=1.6.x"
    "(>=SSE2 CPUs)."
)
_pcsx2_17_optdepends=(
  "pcsx2-1.7:"
    "Support for launching PlayStation 2"
    "videogames with PCSX2>=1.7.x"
    "(>=SSE3 CPUs)."
)
_pcsx2_optdepends=(
  "pcsx2:"
    "Support for launching PlayStation 2"
    "videogames with PCSX2"
    "(>=SSE4 CPUs)."
)
_retroarch_optdepends=(
  "retroarch:"
    "launch videogames"
    "with RetroArch."
)
_retroarch_doom_optdepends=(
  "libretro-prboom:"
    "Support for launching"
    "Doom engine videogames"
    "with PrBoom Retroarch core."
)
_retroarch_dosbox_optdepends=(
  "libretro-dosbox-pure:"
    "Support for launching"
    "DOS videogames"
    "with DOSBox Pure"
    "Retroarch core."
)
_retroarch_fceumm_optdepends=(
  "libretro-fceumm:"
    "Support for launching"
    "Nintendo FamiCom videogames"
    "with RetroArch."
)
_retroarch_flycast_optdepends=(
  "libretro-flycast:"
    "Support for launching"
    "Sega Dreamcast videogames"
    "with RetroArch."
)
_retroarch_nintendo64_optdepends=(
  "libretro-mupen64plus-next:"
    "Support for launching"
    "Nintendo 64 videogames"
    "with RetroArch."
)
_retroarch_pcsx_rearmed_optdepends=(
  "libretro-pcsx-rearmed:"
    "Support for launching"
    "PlayStation videogames"
    "with RetroArch PCSX"
    "ReARMed core."
)
_retroarch_quicknes_optdepends=(
  "libretro-quicknes:"
    "Support for launching"
    "Nintendo Entertainment"
    "System videogames"
    "with RetroArch."
)
_retroarch_snes9x_optdepends=(
  "libretro-snes9x:"
    "Support for launching"
    "Super Nintendo Entertainment"
    "System videogames"
    "with RetroArch."
)
_retroarch_scummvm_optdepends=(
  "libretro-scummvm:"
    "Support for launching SCUMMVM"
    "videogames with RetroArch."
)
_scummvm_optdepends=(
  "scummvm:"
    "Support for launching"
    "videogames with SCUMMVM."
)
_snes9x_optdepends=(
  "snes9x:"
    "Support for launching"
    "Super Nintendo Entertainment"
    "System videogames"
    "with SNES9x."
)
optdepends+=(
  "${_doomretro_optdepends[*]}"
  "${_dosbox_optdepends[*]}"
  "${_duckstation_optdepends[*]}"
  "${_flycast_optdepends[*]}"
  "${_fceux_optdepends[*]}"
  "${_famicom_bios_optdepends[*]}"
  "${_gearboy_optdepends[*]}"
  "${_pcsx2_16_optdepends[*]}"
  "${_pcsx2_17_optdepends[*]}"
  "${_pcsx2_optdepends[*]}"
  "${_retroarch_optdepends[*]}"
  "${_retroarch_doom_optdepends[*]}"
  "${_retroarch_dosbox_optdepends[*]}"
  "${_retroarch_fceumm_optdepends[*]}"
  "${_retroarch_flycast_optdepends[*]}"
  "${_retroarch_nintendo64_optdepends[*]}"
  "${_retroarch_quicknes_optdepends[*]}"
  "${_retroarch_pcsx_rearmed_optdepends[*]}"
  "${_retroarch_scummvm_optdepends[*]}"
  "${_retroarch_snes9x_optdepends[*]}"
  "${_scummvm_optdepends[*]}"
  "${_snes9x_optdepends[*]}"
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
_archive_sum="9a7ec6fe4fa96c457410cf45d5d93732dee0b1f14f5681cb8654097a95f56d72"
_archive_sig_sum="4b7117b3f05e3b65d03154903fd89f4a557dff428bad06b31551e62ab2a2ba02"
_evmfs_ns="0x87003Bd6C074C713783df04f36517451fF34CBEf"
_evmfs_network="100"
_evmfs_address="0x69470b18f8b8b5f92b48f6199dcb147b4be96571"
_evmfs_archive_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_archive_sum}"
_evmfs_archive_src="${_tarname}.tar.gz::${_evmfs_archive_uri}"
_archive_sig_uri="evmfs://${_evmfs_network}/${_evmfs_address}/${_evmfs_ns}/${_archive_sig_sum}"
_archive_sig_src="${_tarname}.tar.gz.sig::${_archive_sig_uri}"
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
    _src="${_tarname}.tar.gz::${_url}/-/archive/${_tag}/${_tarname}.tar.gz"
    _sum="d4f4179c6e4ce1702c5fe6af132669e8ec4d0378428f69518f2926b969663a91"
    _sum="Who cares, fetching stuff using tags with git is unsecure."
  elif [[ "${_tag_name}" == "commit" ]]; then
    if [[ "${_mirror_type}" == "public" ]]; then
      _src="${_tarname}.zip::${_url}/archive/${_commit}.zip"
    elif [[ "${_mirror_type}" == "private" ]]; then
      _src="${_tarname}.tar.gz::${_url}/-/archive/${pkgver}/${_pkg}-${pkgver}.tar.gz"
    fi
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
  # Truocolo
  #   <truocolo@aol.com>
  '97E989E6CF1D2C7F7A41FF9F95684DBE23D6A3E9'
  'DD6732B02E6C88E9E27E2E0D5FC6652B9D9A6C01'
  # Truocolo (kf)
  #   <truocolo@0x6E5163fC4BFc1511Dbe06bB605cc14a3e462332b>
  'F690CBC17BD1F53557290AF51FC17D540D0ADEED'
  # Pellegrino Prevete (dvorak)
  #   <dvorak@0x87003Bd6C074C713783df04f36517451fF34CBEf>
  '12D8E3D7888F741E89F86EE0FEC8567A644F1D16'
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
  install \
    -vDm644 \
    "COPYING" \
    "${pkgdir}/usr/share/licenses/${pkgname}-docs"
}

# vim:set sw=2 sts=-1 et:
