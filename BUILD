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
  hdrs = glob([
    '**/*.h',
  ]),
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
