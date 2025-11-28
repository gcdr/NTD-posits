# NTA2 File Format

## Details

* It is essentially straightforward. There are 78 elements in a 12-column and 12-row number triangle. These are the entries in:

~~~
1 :1
1 :2
1 :3
1 :4
2 :5
1 :6
1 :7
3 :8
3 :9
1 :10
~~~

* See. The top of Pascal's triangle is there.
* The remaining elements 79 to 99 are the entries that allow the filling of extra RSD (Rising Shallow Diagonal) elements — shown in the picture below.

![Addon Lower Left Number Triangle](https://github.com/gcdr/NTD-posits/blob/main/images/lower-triangle2.jpg)

* The remaining elements, as indicated in the graphic, correspond to those particular values.

~~~
16 :98
1 :99
  
RSD Values: 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987
RS Values: 1 2 4 8 16 32 64 128 34 256 512 1024 2048

RSD Odd: 1 3 8 21 55 144 377 987
RSD Even: 1 2 5 13 34 89 233 610

RS Odd: 2 8 32 128 512 2048
RS Even: 1 4 16 64 256 1024
~~~

* The bottom values are only written when saving.
* They are not read upon loading. i.e., The RSD Values to RS Even `values`.
* RSD: Rising Shallow Diagonal (Sums)
* RS: Row Sums
* Odd values are the odd bisection of the RSD or RS sequences computed from the number triangle.
* Why do this? Several number triangles are connected to sequences by one or the other bisection of their two-sum sequences.

## Preview of NTA2

* Here is a screen shot of the actual application.

![NTA2 Application Image](https://github.com/gcdr/NTD-posits/blob/main/images/full-NTA2.jpg)