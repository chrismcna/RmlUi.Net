```


--------- Windows build 
git submodule update --init --recursive

cd mkdir build && cd build

cmake .. -DCMAKE_GENERATOR_PLATFORM=win32 -DCMAKE_SYSTEM_PROCESSOR=x86 -DCMAKE_BUILD_TYPE=Debug
cmake --build .
cp ../bin/Debug/RmlUiNative.dll ../../RmlUI.Net/runtimes/win-x86/native/RmlUiNative.dll


--------- Linux build
docker run -it -v C:\Users\ChrisMcnamee\source\repos\RmlUi.Net\RmlUi.Native:/native --platform=linux/arm64/v8 --rm -it arm64v8/ubuntu  
apt update
apt install build-essential libsdl2-dev cmake


mkdir /native/build && cd /native/build

cmake .. -DCMAKE_BUILD_TYPE=Debug
cmake --build .





cmake .. -DCMAKE_TOOLCHAIN_FILE=Toolchain_aarch64_l4t.cmake


CC=arm-linux-gnueabihf-gcc 
cmake .. -DCMAKE_CXX_COMPILER=arm-linux-gnueabi-gcc -DCMAKE_BUILD_TYPE=Debug

cmake .. -DCMAKE_BUILD_TYPE=Debug
cmake --build .


```






