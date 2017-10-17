apple_library(
  name = 'BugSample',
  visibility = ['PUBLIC'],
  exported_headers = glob([
  ]),
  srcs = glob([
    'BugSample/*.swift'
  ]),
  deps = [
    '//Pods:PromiseKit',
  ],
)

apple_binary(
  name = 'BugSampleBinary',
  visibility = ['PUBLIC'],
  deps = [
    # main binary
    ':BugSample',

    # assets
    ':BugSampleAssets',

    # resource
    ':BugSampleResources',
  ],
)

apple_bundle(
  name = 'BugSampleApp',
  product_name = 'BugSample',
  binary = ':BugSampleBinary',
  extension = 'app',
  info_plist = 'BugSample/Info.plist',
)

apple_asset_catalog(
  name = 'BugSampleAssets',
  dirs = [
    'BugSample/Assets.xcassets',
  ]
)

apple_resource(
  name = 'BugSampleResources',
  visibility = ['PUBLIC'],
  files = glob([
    'BugSample/Base.lproj/*.*',
  ]),
  dirs = [
    'BugSample/Base.lproj',
  ],
)
