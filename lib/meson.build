
lz4_inc = [include_directories('.')]
lz4_cargs = ['-Wall', '-Werror']
lz4_src = [
    'lz4.c',
    'lz4hc.c',
    'lz4frame.c',
    'xxhash.c',
]
lz4_lib = static_library(
    'lz4',
    lz4_src,
    include_directories: lz4_inc,
    pic: true,
    c_args: lz4_cargs,
)
lz4_dep = declare_dependency(
    include_directories: lz4_inc,
    link_with: lz4_lib,
)
