licenses(['notice'])

config_setting(
  name = 'darwin',
  values = {
    'cpu': 'darwin',
  }
)

cc_library(
  name = 'glog',
  visibility = ['//visibility:public'],
  deps = [
    '//external:gflags'
  ],
  hdrs = [
    '__build__/darwin/src/config.h',
    '__build__/linux/src/config.h',
    'src/demangle.h',
    'src/utilities.h',
    'src/base/commandlineflags.h',
    'src/base/googleinit.h',
    'src/base/mutex.h',
    'src/glog/log_severity.h',
    'src/symbolize.h',
    'src/stacktrace.h',
    'src/stacktrace_x86_64-inl.h',
  ],
  srcs = [
    'src/demangle.cc',
    'src/logging.cc',
    'src/raw_logging.cc',
    'src/signalhandler.cc',
    'src/symbolize.cc',
    'src/utilities.cc',
    'src/vlog_is_on.cc',
  ],
  includes = [
    'include'
  ],
  copts = select({
    ':darwin': ['-iquoteglog/__build__/darwin/src'],
    '//conditions:default': ['-iquoteglog/__build__/linux/src'],
  }) + ['-iquoteglog/src'],
)
