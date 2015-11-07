import os.path
import sys

env = Environment(ENV = {'PATH' : os.environ['PATH'],
                         'HOME' : os.environ['HOME']})
env.Append(CCFLAGS = ['-g', '-O0', '-ggdb', '-std=c++11'])

AddOption('--some_build_script',
          action='store_true',
          help='some build script explanation',
          default=False)

if GetOption('some_build_script'):
	build_dir = 'build/some_build_script'
	SConscript('some_build_script_SConscript', variant_dir=build_dir, src_dir='src', duplicate=0, exports=['env'])

else:
	print("USE FLAG FROM THE RANGE: --some_build_script")