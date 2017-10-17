apple_binary(
  name = 'BugSampleBinary',
  visibility = ['PUBLIC'],
  swift_version = '3',
  modular = True,
  srcs = glob([
    'BugSample/main.m',
    'BugSample/*.swift',
  ]),
  deps = [
    # main binary
    '//Pods:PromiseKit',

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
