project('windows_pdb_reproducer', 'c', version: '0.1')

src_files = files('main.c')
pch_file = meson.project_source_root() / 'pch.h'

shared_lib = shared_library(
  'mylib',
  src_files,
  install: true,
  name_prefix: '',
)

static_lib = static_library(
  'mylib',
  src_files,
  install: true,
  c_pch: pch_file,
  name_prefix: '',
)

# meson setup --backend ninja --buildtype debug -Dc_link_args=/DEBUG:FASTLINK build && ninja -C build
