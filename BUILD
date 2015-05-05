licenses(['notice'])

cc_library(
  name = 'glog',
  visibility = ['//visibility:public'],
  deps = [
    '//external:gflags'
  ],
  hdrs = [
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
    '__build__/linux/src',
    'src',
  ],
)
