licenses(['notice'])

package(default_visibility = ['//visibility:public'])

cc_library(
  name = 'boost',
  deps = [
    ':atomic',
    ':chrono',
    ':context',
    ':date_time',
    ':filesystem',
    ':regex',
    ':system',
    ':thread',
  ],
  hdrs = glob([
    'boost/*.h',
  ]),
  srcs = [
  ],
  linkstatic = 1,
)

cc_library(
  name = 'atomic',
  deps = [
    ':system',
  ],
  srcs = [
    'libs/atomic/src/lockpool.cpp',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'chrono',
  deps = [
    ':system',
  ],
  srcs = [
    'libs/chrono/src/chrono.cpp',
    'libs/chrono/src/process_cpu_clocks.cpp',
    'libs/chrono/src/thread_clock.cpp'
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'context',
  srcs = [
    'libs/context/src/asm/jump_x86_64_sysv_elf_gas.S',
    'libs/context/src/asm/make_x86_64_sysv_elf_gas.S',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'date_time',
  deps = [
    ':system',
  ],
  srcs = [
    'libs/date_time/src/gregorian/date_generators.cpp',
    'libs/date_time/src/gregorian/greg_month.cpp',
    'libs/date_time/src/gregorian/gregorian_types.cpp',
    'libs/date_time/src/gregorian/greg_weekday.cpp',
    'libs/date_time/src/posix_time/posix_time_types.cpp',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'filesystem',
  deps = [
    ':system',
  ],
  srcs = [
    'libs/filesystem/src/codecvt_error_category.cpp',
    'libs/filesystem/src/operations.cpp',
    'libs/filesystem/src/path.cpp',
    'libs/filesystem/src/path_traits.cpp',
    'libs/filesystem/src/portability.cpp',
    'libs/filesystem/src/unique_path.cpp',
    'libs/filesystem/src/utf8_codecvt_facet.cpp',
    'libs/filesystem/src/windows_file_codecvt.cpp',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'regex',
  deps = [
    ':system',
  ],
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
    'libs/regex/src/winstances.cpp'
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  linkopts = [
    '-pthread',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'system',
  srcs = [
    'libs/system/src/error_code.cpp',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  includes = [
    '.',
  ],
  alwayslink = 1,
  linkstatic = 1,
)

cc_library(
  name = 'thread',
  deps = [
    ':system',
  ],
  srcs = [
    'libs/thread/src/future.cpp',
    'libs/thread/src/tss_null.cpp',
    'libs/thread/src/pthread/once_atomic.cpp',
    'libs/thread/src/pthread/thread.cpp',
  ],
  includes = [
    '.',
  ],
  defines = [
    'BOOST_ALL_STATIC_LINK=1'
  ],
  linkopts = [
    '-pthread',
  ],
  alwayslink = 1,
  linkstatic = 1,
)
