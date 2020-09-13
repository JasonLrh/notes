> #include <opencv2/opencv.hpp>  
#include <opencv2/highgui.hpp>  
#include <opencv2/video.hpp>  
#include <opencv2/core.hpp>  
#include <opencv2/imgproc.hpp>  
#include <opencv2/imgcodecs.hpp>  
...

> using namespace cv;  

## GUI

cv::`namedWindow` `("window name",WINDOW_AUTOSIZE)`;  
cv::`imshow` `("window name",src)`;

## 数据类

cv::`Mat`
> `Mat` src = `imread` `("filePath",IMREAD_COLOR)`;  
> `imwrite` `("filePath",src)`;  

## 时间度量

> `double` t = (`double`)`getTickCount`();  
> ...  
> t = (`getTickCount`()-t)/`getTickFrequency`();  

(t ,单位:秒)