import sys

cc_library(
  name = 'boost',
  deps = [
    ':chrono',
    ':cpp-netlib',
    ':filesystem',
    ':iostreams',
    ':regex',
    ':system',
    ':thread',
  ]
)

cc_library(
  name = 'boost_headers',
  export_incs = [
    '.',
  ]
)

cc_library(
  name = 'chrono',
  warning = 'no',
  srcs = [
    'libs/chrono/src/chrono.cpp',
    'libs/chrono/src/process_cpu_clocks.cpp',
    'libs/chrono/src/thread_clock.cpp'
  ],
  deps = [
    ':boost_headers',
    ':system',
  ],
)

cc_library(
  name = 'cpp-netlib',
  deps = [
    '//thirdparty/cpp-netlib-0.11.0-final:cpp-netlib'
  ]
)

cc_library(
  name = 'filesystem',
  warning = 'no',
  srcs = [
    'libs/filesystem/src/codecvt_error_category.cpp',
    'libs/filesystem/src/operations.cpp',
    'libs/filesystem/src/path.cpp',
    'libs/filesystem/src/path_traits.cpp',
    'libs/filesystem/src/portability.cpp',
    'libs/filesystem/src/unique_path.cpp',
    'libs/filesystem/src/utf8_codecvt_facet.cpp',
    'libs/filesystem/src/windows_file_codecvt.cpp'
  ],
  deps = [
    ':boost_headers',
    ':system',
  ],
)

cc_library(
  name = 'iostreams',
  srcs = [
    'libs/iostreams/src/bzip2.cpp',
    'libs/iostreams/src/file_descriptor.cpp',
    'libs/iostreams/src/gzip.cpp',
    'libs/iostreams/src/mapped_file.cpp',
    'libs/iostreams/src/zlib.cpp'
  ],
  deps = [
    ':boost_headers',
    '//thirdparty/bzip2:bz2',
    '//thirdparty/zlib:zlib',
  ]
)

python_version = str(sys.version_info[0]) + "." + str(sys.version_info[1])

cc_library(
  name = 'python',
  srcs = [
    'libs/python/src/converter/arg_to_python_base.cpp',
    'libs/python/src/converter/builtin_converters.cpp',
    'libs/python/src/converter/from_python.cpp',
    'libs/python/src/converter/registry.cpp',
    'libs/python/src/converter/type_id.cpp',
    'libs/python/src/object/class.cpp',
    'libs/python/src/object/enum.cpp',
    'libs/python/src/object/function.cpp',
    'libs/python/src/object/function_doc_signature.cpp',
    'libs/python/src/object/inheritance.cpp',
    'libs/python/src/object/iterator.cpp',
    'libs/python/src/object/life_support.cpp',
    'libs/python/src/object/pickle_support.cpp',
    'libs/python/src/object/stl_iterator.cpp',
    'libs/python/src/dict.cpp',
    'libs/python/src/errors.cpp',
    'libs/python/src/exec.cpp',
    'libs/python/src/import.cpp',
    'libs/python/src/list.cpp',
    'libs/python/src/long.cpp',
    'libs/python/src/module.cpp',
    'libs/python/src/numeric.cpp',
    'libs/python/src/object_operators.cpp',
    'libs/python/src/object_protocol.cpp',
    'libs/python/src/slice.cpp',
    'libs/python/src/str.cpp',
    'libs/python/src/tuple.cpp',
    'libs/python/src/wrapper.cpp'
  ],
  deps = [
    '#python' + python_version,
    ':boost_headers',
  ]
)

cc_library(
  name = 'regex',
  srcs = [
    'libs/regex/src/cpp_regex_traits.cpp',
    'libs/regex/src/cregex.cpp',
    'libs/regex/src/c_regex_traits.cpp',
    'libs/regex/src/fileiter.cpp',
    'libs/regex/src/icu.cpp',
    'libs/regex/src/instances.cpp',
    'libs/regex/src/posix_api.cpp',
    'libs/regex/src/regex.cpp',
    'libs/regex/src/regex_debug.cpp',
    'libs/regex/src/regex_raw_buffer.cpp',
    'libs/regex/src/regex_traits_defaults.cpp',
    'libs/regex/src/static_mutex.cpp',
    'libs/regex/src/usinstances.cpp',
    'libs/regex/src/w32_regex_traits.cpp',
    'libs/regex/src/wc_regex_traits.cpp',
    'libs/regex/src/wide_posix_api.cpp',
    'libs/regex/src/winstances.cpp',
  ],
  deps = [
    ':boost_headers',
  ]
)

cc_library(
  name = 'system',
  warning = 'no',
  srcs = [
    'libs/system/src/error_code.cpp',
  ],
  deps = [
    '#rt',
    ':boost_headers',
  ],
)

cc_library(
  name = 'thread',
  warning = 'no',
  srcs = [
    'libs/thread/src/future.cpp',
    'libs/thread/src/tss_null.cpp',
    'libs/thread/src/pthread/once_atomic.cpp',
    'libs/thread/src/pthread/thread.cpp',
  ],
  deps = [
    '#pthread',
    ':boost_headers',
    ':system',
  ],
)
