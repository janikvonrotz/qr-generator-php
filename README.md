# About

This program outputs a QRcode as either a PNG, JPEG, or GIF.
Max image size of 1480*1480 pixels.

Supports QRcode version 1-40.

Requires PHP4.1 and gd 1.6 or higher.

# Usage

qr.php?  
d=[data]  
&e=[(L,M,Q,H)]  
&s=[int]  
&v=[(1-40)]  
&t=[(J,G)]  
&size=[int]  
&download=[filename]  

## experimental

&m=[(1-16)]  
&n=[(2-16)]  
&p=[(0-255)]  
&o=[data]  

# Parameter

* d = data URL encoded data.
* e = ECC level: L or M or Q or H (default M)
* s = module size (dafault PNG:4 JPEG:8)
* v = version 1-40 or Auto select if you do not set.
* t = image type J: jpeg image, G: GIF image, default: PNG image
* size = image size Integer. Specifies the width & height of the image. Default 400. Max 1480.
* download = File name URL encoded filename. If set, the content disposition will change to tell the browser to download the file.

# Example

`index.php?d=hello&e=Q&t=J&size=500&download=test`

Will encode a QR code containin the word "hello" with Quartile error correction, as a JPG, 500px wide & high, and prompt you to download it as a file called "test.jpg".

## Experimental Parameter

structured append  m of n (experimental):

* n = structure append n (2-16)
* m = structure append m (1-16)
* p = parity
* o = original data (URL encoded data)  for calculating parity

# License

Original version (C)2000-2009,Y.Swetake (version 0.50i)
From: http://www.venus.dti.ne.jp/~swe/program/qr_img0.50i.tar.gz
http://www.swetake.com/qr/
Licenced as "revised BSD License" by the original author
	
Subsequent Changes
Copyright (c) 2012, Terence Eden
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:
* Redistributions of source code must retain the above copyright notices, this list of conditions and the following disclaimer.
* Redistributions in binary form must reproduce the above copyright notices, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.
* Neither the name of the software nor the names of its contributors may be used to endorse or promote products derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER(S) BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

The QR code standard is trademarked by Denso Wave, Inc.
http://www.denso-wave.com/qrcode/index-e.html
