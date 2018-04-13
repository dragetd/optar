project('optar', 'c',
	version : '1.0',
	default_options : ['warning_level=3', 'cpp_std=c++11'])

incdir = include_directories('src')
deps = dependency('libpng')
m_dep = meson.get_compiler('c').find_library('m', required : false)

executable('optar', sources : ['src/optar.c', 'src/common.c', 'src/parity.c', 'src/golay_codes.c'], include_directories : incdir)
executable('unoptar', sources : ['src/unoptar.c', 'src/common.c', 'src/parity.c', 'src/golay_codes.c'], include_directories : incdir, dependencies : [deps, m_dep])
executable('golay', sources : ['src/golay.c', 'src/parity.c'], include_directories : incdir)
