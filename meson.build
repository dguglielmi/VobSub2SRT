project('vobsub2srt', 'cpp', 'c',
  version : '1.0pre7',
  license: [ 'GPL3+' ],
   meson_version : '>= 0.50.0'
)

subdir('src')
subdir('third_party')
subdir('docs')

threads_dep = dependency('threads',
  required : true
)

tesseract_dep = dependency('tesseract',
  method : 'pkg-config',
  version : '>=4.1.0',
  required : true
)

vobsub2srt_bin_deps = [ threads_dep,
  tesseract_dep ]

vobsub2srt_bin = executable('vobsub2srt',
  sources : vobsub2srt_sources,
  dependencies : vobsub2srt_bin_deps,
  link_with : mplayer_vobsub_lib,
  install : true
)
