# define the project
project(
    'nn.h',
    'c',
    default_options: [
        'buildtype=release',
        'optimization=3',
        'strip=true',
        'b_ndebug=if-release',
    ],
    version: '1.0.0',
    license: 'MIT',
)

# get the math library, this also takes care of cases, where there is no dynamic math library e.g. windows msvc
cc = meson.get_compiler('c')
math_dep = cc.find_library('m', required: true)

# get the raylib library, tries to get it from the system, if not bild it from scratch, this also takes care of flags that raylib needs e.g pthread
raylib_proj = subproject('raylib')
raylib_dep = raylib_proj.get_variable('raylib_dep')

# add include folders
incs = []
incs += include_directories('./thirdparty')


executable_settings = [
    'warning_level=3',
    'werror=true',
]

# define all executables
executable(
    'adder_gen',
    'adder_gen.c',
    dependencies: [math_dep],
    include_directories: incs,
    override_options: executable_settings,
)

executable(
    'xor',
    'xor.c',
    dependencies: [raylib_dep],
    include_directories: incs,
    override_options: executable_settings,
)

executable(
    'gym',
    'gym.c',
    dependencies: [raylib_dep],
    include_directories: incs,
    override_options: executable_settings,
)

executable(
    'img2nn',
    'img2nn.c',
    dependencies: [raylib_dep],
    include_directories: incs,
    override_options: executable_settings,
)
