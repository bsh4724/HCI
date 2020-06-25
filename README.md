# HCI final report 1-3
## Increasing interaction between teacher-student of online learning using hand detection and face recognition in webcam
#### 21600259 박성경, 21700326 반수현, 21700729 최슬기, 21800639 장하리
### (1) Introduction 
#### - Background and goal of our research
> 코로나 사태로 인해 초등학교부터 대학교까지 많은 학교들이 온라인 수업으로 학기를 진행했다. 그러나 대면수업과는 달리 온라인 수업은 학생과 교사의 상호작용적인 수업이 아닌, 수업화면과 수업에 기반인 수업이 진행되었다. 그래서 기존 수업과는 달리 학생들과 교사들 사이의 상호작용이 원활하지 않다는 문제점을 발견하고, 이를 해소하기 위해 컴퓨터와 노트북에 흔히 내장되어 있는 웹캠을 이용하여 교사와 학생간의 상호작용을 높이고자 하였다. 내장된 웹캠을 손 인식과 얼굴 랜드마크 인식 기능을 이용할 것이다.
학생과 교사의 상호작용의 부족함을 해소하기 위해, 우리 조는 학생들의 집중도를 높일 수 있게 도와줄 시각적 효과와 교사들이 학생들의 집중도와 이해도를 알 수 있는 척도를 제공해주는 것이 목표이다. 

--------------------------------------------------------------------

### (2) Main contents
#### - How to build our program
> we use hand detection and face landmarks openCV and PyQt5 to build our program

![2-1](https://user-images.githubusercontent.com/55008782/85679573-7d68e500-b704-11ea-9e1f-534be0d5bd27.png)

-----------------------------------------------------
#### - Paper prototype

> we have two version of paper prototype, teachers and students

![3-1](https://user-images.githubusercontent.com/55008782/85683676-67f5ba00-b708-11ea-8855-7e104e065863.png)

---------------------------------------------------------------
![3-2](https://user-images.githubusercontent.com/55008782/85683692-6c21d780-b708-11ea-8958-55469264b93b.png)

------------------------------------

![3-3](https://user-images.githubusercontent.com/55008782/85683702-6d530480-b708-11ea-9962-0a152cc75262.png)

---------------------------------------------------------------------------------------------
![3-4](https://user-images.githubusercontent.com/55008782/85683708-6f1cc800-b708-11ea-8f3b-e34704bdf976.png)

--------------------------------------------------------------------------------
![3-5](https://user-images.githubusercontent.com/55008782/85683713-704df500-b708-11ea-94d7-99cf87d91c0b.png)

-----------------------------------------------------


#### - Explanation of source code

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

