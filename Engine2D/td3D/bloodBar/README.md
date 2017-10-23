本例中，血条与掉血的特效均是由egret的2D功能绘制的。

血条的显示位置，应该是跟随人物的。与此类似的还有掉血数字的显示。

![xx](./pic5.png)

进行2D渲染时，采用的是2D坐标系统。而进行3D渲染时，采用的是3D场景的世界坐标。这里需要把3D世界的坐标对应到2D中来：

````
camera.object3DToScreenRay(vec3);
````

可以通过监听ENTER_FRAME事件来实现实时更新，保证血条或掉血特效跟随人物。