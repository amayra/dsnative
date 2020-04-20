# dsnative
Direct Show Binary Codec Loader and Decoder

Direct Show Native Wrapper
dsnative it's a c++ wrapper using MS baseclasses that loads directly a direct show filter, and makes possible decoding of video frames without need for build a directshow application or a Graph. Now only used in MPlayer.

The binary dll should be in the path, alternatively dsnative will try to search the path using Windows registry if the codec is registered in the system.
The sender filter implements IFileSourceFilter so the decoder filter (ffdshow does it) can query GetCurFile() to retrieve the path of currently played media and detect for example subtitles in source file's directory.
The wrapper is made for MPlayer/MEncoder, but teorically it can be used easily in other projects, contact me if interested.

Please note this code is still experimental, I'm not a DirectShow guru, and I'm using DirectShow in a way that is not supposed to be used. It may crash, have weird performances, or crash your pc (unlikely). Framedrop does not always work as expected.

If you have a good knowledge of DirectShow, I would appreciate a lot your help, please contact me.

Direct Show Native Wrapper is licensed under the terms of GNU LGPL v2.1
No binaries are availables here, dsnative dll is bundled with MPlayer package, this will change when the API will be more defined.
