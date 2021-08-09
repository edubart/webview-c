CFLAGS=-Wall
LIN_CC=gcc
LIN_LDFLAGS=`pkg-config --cflags --libs gtk+-3.0 webkit2gtk-4.0`
WIN_LDFLAGS=-lole32 -lcomctl32 -loleaut32 -luuid -lgdi32
WIN_CC=x86_64-w64-mingw32-gcc
WEBVIEW_ENV=WEBVIEW2_WIN32_PATH="`pwd`/../ms.webview2/x64"

test-windows:
	$(WIN_CC) webview-example.c -o webview-example.exe -I.. $(CFLAGS) $(WIN_LDFLAGS)
	$(WEBVIEW_ENV) ./webview-example.exe
	$(WIN_CC) webview-example-2.c -o webview-example2.exe -I.. $(CFLAGS) $(WIN_LDFLAGS)
	$(WEBVIEW_ENV) ./webview-example2.exe

test-linux:
	$(LIN_CC) webview-example.c -o webview-example -I.. $(CFLAGS) $(LIN_LDFLAGS)
	./webview-example
	$(LIN_CC) webview-example-2.c -o webview-example2 -I.. $(CFLAGS) $(LIN_LDFLAGS)
	./webview-example2

