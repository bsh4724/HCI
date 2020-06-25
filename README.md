# HCI final report 1-3
## Increasing interaction between teacher-student of online learning using hand detection and face recognition in webcam
#### 21600259 박성경, 21700326 반수현, 21700729 최슬기, 21800639 장하리
### (1) Introduction 
#### - Background and goal of our research
> Due to COVID 19's global trend, many schools and universities offer online classes. However, since online classes are currently centered on lectures, they have not enough interaction between students and teachers. Through this problem, out team decided to find and apply measures to stimulate insufficient interaction. As a method of activating interaction, the built-in webcam of the laptop and the desktop computer will be used with hand detection and face recognition.
To resolve lack of interaction between teachers and students,  we aim to raise students’ concentration by using visual effects to encourage students. also, we aim to enable teachers to know students’ concentration and understanding during lectures. 

--------------------------------------------------------------------

### (2) Main contents
#### - How to build our program
> we use hand detection and face landmarks openCV and PyQt5 to build our program

![2-1](https://user-images.githubusercontent.com/55008782/85679573-7d68e500-b704-11ea-9e1f-534be0d5bd27.png)


#### - Paper prototype

> we have two version of paper prototype, teachers and students

![3-1](https://user-images.githubusercontent.com/55008782/85683676-67f5ba00-b708-11ea-8855-7e104e065863.png)
![3-2](https://user-images.githubusercontent.com/55008782/85683692-6c21d780-b708-11ea-8958-55469264b93b.png)

![3-3](https://user-images.githubusercontent.com/55008782/85683702-6d530480-b708-11ea-9962-0a152cc75262.png)
![3-4](https://user-images.githubusercontent.com/55008782/85683708-6f1cc800-b708-11ea-8f3b-e34704bdf976.png)
![3-5](https://user-images.githubusercontent.com/55008782/85683713-704df500-b708-11ea-94d7-99cf87d91c0b.png)

---------------------------------------------------------------------------------------------------------------

#### Explanation of source code

1. git에서 해당되는 소스파일을 clone 해온다.
```
git clone https://github.com/csg17/HCI
```

2. 사용한 오픈소스 github주소에 들어가서 필요한 것들을 다운받는다.
> https://github.com/jaredvasquez/CNN-HowManyFingers
> > img.tgz와 model_6cat.h5를 다운받아서 finger_counting에 넣어준다.

> https://www.pyimagesearch.com/2017/05/08/drowsiness-detection-opencv/
> > shape_predictor_68_landmarks.dat을 다운받아서 drowsiness&sleep폴더에 넣어준다.

3. pyqt 설치하기.
> https://mainia.tistory.com/5604

4. 총 3가지의 폴더가 다운로드 받아진다. (drowsiness&sleep, zoom_version2_pyqt2, finger_counting)
> 졸거나 하품할 때 알림이 나오는 코드를 실행하려면 drowsiness&sleep을 들어간다.
```
cd drowsiness&sleep
python drowsiness_sleep.py --shape-predictor shape_predictor_68_landmarks.dat --alarm alarm.wav
```

> 가상의 온라인 학습 창을 실행하기 위해서는 zoom_version2_pyqt 를 들어간다.
```
cd zoom_version2_pyqt
python app.py
```

>손가락을 counting 해주고 정답인지 아닌지 알려주는 코드를 실행하려면 finger_counting을 들어간다. 
```
cd finger_counting
python application.py
```

------------------------------------------------------------------------------
