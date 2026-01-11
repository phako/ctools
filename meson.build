project(
  'ctool',
  'cpp',
  version : '0.4',
  meson_version : '>= 1.3.0',
  default_options : ['optimization=2', 'warning_level=everything', 'cpp_std=c++23'],
)

add_project_arguments('-DVERSION="@0@"'.format(meson.project_version()), language: 'cpp')

ctools_lib = static_library('ctools-lib',
  [
    'src/bios.cc',
    'src/bitstr.cc',
    'src/d64.cc',
    'src/dir.cc',
    'src/dump.cc',
    'src/err.cc',
    'src/fcb.cc',
    'src/file.cc',
    'src/misc.cc',
    'src/tools.cc',
  ]
)

executable(
  'ctools',
  'src/ctools.cc',
  install : true,
  link_with: ctools_lib,
)

executable(
  'd64dump',
  'src/d64dump.cc',
  install: true,
  link_with: ctools_lib,
)

executable(
  'biosdump',
  'src/biosdump.cc',
  install:true,
  link_with: ctools_lib,
)

executable(
  'cformat',
  'src/cformat.cc',
  install:true,
  link_with: ctools_lib
)
