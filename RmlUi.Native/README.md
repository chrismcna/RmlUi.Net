```


--------- Windows build 
git submodule update --init --recursive

cd mkdir build && cd build

cmake .. -DCMAKE_GENERATOR_PLATFORM=win32 -DCMAKE_SYSTEM_PROCESSOR=x86 -DCMAKE_BUILD_TYPE=Debug
cmake --build .
cp ../bin/Debug/RmlUiNative.dll ../../RmlUI.Net/runtimes/win-x86/native/RmlUiNative.dll


--------- Linux build
docker run -it -v RmlUi.Net\RmlUi.Native:/native amd64/ubuntu:rolling
apt update
apt install build-essential libsdl2-dev
apt install cmake

cd /native

mkdir build && cd build

cmake .. -DCMAKE_CXX_COMPILER=g++ -DCMAKE_BUILD_TYPE=Debug
cmake --build .


```






