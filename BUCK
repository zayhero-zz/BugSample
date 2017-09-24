apple_binary(
    name = 'SwiftCallsObjC',
    srcs = [
       'main.swift'
    ],
    frameworks = [
        '$SDKROOT/System/Library/Frameworks/Foundation.framework'
    ],
    bridging_header = 'bridging-header.h',
    deps = [':Greeter'],
)

apple_library(
    name = 'Greeter',
    srcs = [
        'Greeter.m'
    ],
    exported_headers = [
        'Greeter.h'
    ]
)

apple_test(
    name = 'GreeterTest',
    info_plist = 'Info.plist',
    srcs = [
        'Greeter.m',
        'sample.swift',
    ],
    exported_headers = [
        'Greeter.h'
    ]
)
