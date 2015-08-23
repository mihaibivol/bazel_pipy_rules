load('/build_defs/python_external', 'python_package_lib')
load('/build_defs/python_external', 'python_package_bundle')

python_package_lib(
    name = 'marisa_trie',
    dep = '@marisa_trie//:files',
    visibility = ['//visibility:public']
)

python_package_lib(
    name = 'ipdb',
    dep = '@ipdb//:files',
    visibility = ['//visibility:public']
)

python_package_bundle(
    name = 'external',
    deps = [
        '@ipdb//:files',
        '@marisa_trie//:files',
    ],
    visibility = ['//visibility:public']
)
