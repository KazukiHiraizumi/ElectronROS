# ElectronROS
Ros frontend framework build by Electron

## Electronのインストール
~~~
npm install electron
~~~
~/node_modules/electron/dist/electronに/usr/local/bin/electronからリンクしておこう。
~~~
sudo ln -fs ~/node_modules/electron/dist/electron /usr/local/bin/electron
~~~

## ROS WEB TOOL
ROSのWEBツールは

http://robotwebtools.org/

に沢山ある。paramanに要りそうなものは・・・

1. rosbridge_server
~~~
sudo apt-get install ros-kinetic-rosbridge-server
~~~

2. roslibjs
~~~
curl https://static.robotwebtools.org/roslibjs/current/roslib.min.js >roslib.js
~~~

3. フロントエンド用EventEmitter
~~~
curl https://static.robotwebtools.org/EventEmitter2/current/eventemitter2.min.js >event_emitter.js
~~~

## Test Run

1. サンプルパラメータをロード
~~~
roscd rovi
rosparam load yaml/ycam3vga.yaml
~~~

2. rosbridge_serverを起動
~~~
roslaunch rosbridge_server rosbridge_websocket.launch
~~~

3. アプリ起動
~~~
electron <application folder>
~~~

## 配布
