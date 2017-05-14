---

title: QT构建错误：error: expected ';'
subtitle: QT构建错误：error: expected ';'
date: 2017-05-12 19:51:39
author: 谢孟辉
tags:
	- QT
categories: 
	- CS
	
---

## QT构建错误：error: expected ';' at end of declaration list

![QTErrorExpected](http://ojlsgreog.bkt.clouddn.com/QTErrorExpected.jpg)


	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_io/AsciiFilter.cpp:18:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_io/AsciiFilter.h:21:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_io/FileIOFilter.h:22:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_db/ccHObject.h:22:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_db/ccObject.h:22:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_db/ccSerializableObject.h:22:
	In file included from ../../../../InnerEyes/CloudCompare/libs/qCC_db/ccLog.h:29:
	In file included from /Users/xx/Applications/Qt5.8.0/5.8/clang_64/lib/QtCore.framework/Headers/QString:1:
	In file included from /Users/xx/Applications/Qt5.8.0/5.8/clang_64/lib/QtCore.framework/Headers/qstring.h:50:
	/Users/xx/Applications/Qt5.8.0/5.8/clang_64/lib/QtCore.framework/Headers/qrefcount.h:54:22: error: expected ';' at end of 	declaration list
    	inline bool ref() Q_DECL_NOTHROW {
                     	^
                     	;
                     	
## qt5 keg-only

	brew unlink qt
	brew link --force qt5
	cmake -DCMAKE_PREFIX_PATH:STRING=/usr/local/opt/qt5/lib/cmake/ ..
	make install
	brew unlink qt5
	brew link qt
	
[Github . Build fails on OS X, seems to be related to Qt5](https://github.com/miek/inspectrum/issues/60)
               

## brew unlink qt

	brew unlink qt
	
![QTErrorNoRule](http://ojlsgreog.bkt.clouddn.com/QTErrorNoRule.jpg)
	