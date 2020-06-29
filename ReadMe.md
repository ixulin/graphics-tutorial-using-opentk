## 目标
1. 了解渲染基本原理 
2. 了解游戏引擎的基本逻辑
3. 用原始图形API实现自己的游戏demo 


## 第一课：用顶点绘制三角形（5小时)
1. 用opentk打开opengl窗口（1小时）
    - Tips
        > 说明：Tips为遇到问题时可提供的参考，请自己先思考、实践之后再看，以下雷同
        - http://neokabuto.blogspot.com/2013/02/opentk-tutorial-1-opening-windows-and.html
        - 自行搜索OpenTK
        - 理解窗口、缓冲区概念

2. 用顶点绘制最简单的三角形（4小时）
    - 需要关注的接口
        > 说明：因为可以有很多种实现最后结果的方式，所以以下这些接口不一定非要用到，也不保证只会使用到下列接口；为提高学习效用，请先自行查找相关API，以下雷同
        - GL.Clear
        - Matrix4.CreatePerspectiveFieldOfView
        - Matrix4.LookAt
    - Tips
        - 理解“OpenGL是一个状态机”
        - Model矩阵、View矩阵、Projection矩阵、Viewport
        - https://learnopengl-cn.github.io/01%20Getting%20started/07%20Transformations/
        - https://learnopengl-cn.github.io/01%20Getting%20started/08%20Coordinate%20Systems/
        - GL.Vertex3()、GL.Color()

## 第二课：利用缓冲区对象替换GL.Vertex3()绘制之前的三角形
1. 理解关于顶点绘制的各种缓冲区对象（2小时）
    - Tips
        - VAO、VBO、EBO
        - 理解顶点和索引的区别
        - https://opentk.net/learn/chapter1/2-hello-triangle.html
        - https://learnopengl-cn.github.io/01%20Getting%20started/04%20Hello%20Triangle/
2. 利用缓冲区对象替换GL.Vertex3()绘制之前的三角形（6小时）
    - 相关接口
        - GL.GenBuffers
        - GL.BindBuffer
        - GL.BufferData
        - GL.DrawArray 或者 GL.DrawElement


## 第三课:使用着色器绘制三角形
1. 了解如何载入并使用shader（1小时）
    - 相关接口
        - GL.CreateProgram
        - GL.CompileShader
        - GL.AttachShader
2. 使用shader来绘制三角形（6小时）
    - Tips
        - 属性绑定点: 如何将应用程序中的数据传入shader？
        - 属性传递：Application -> Vertex -> Fragment
        - http://neokabuto.blogspot.com/2013/03/opentk-tutorial-2-drawing-triangle.html
        - https://opentk.net/learn/chapter1/2-hello-triangle.html
        - https://learnopengl-cn.github.io/01%20Getting%20started/04%20Hello%20Triangle/
    - 相关接口
        - GL.BufferData
        - GL.VertexAttribPointer

## 第四课：封装
1. 重构之前的代码（6小时）
    - 封装Shader类
    - 抽离Geometry类
    - 实现Camera类
2. 新建自己的场景，并创建相机围绕场景旋转（2小时）
    - Tips
        - http://neokabuto.blogspot.com/2014/01/opentk-tutorial-5-basic-camera.html

## 第五课：支持Obj格式
1. 弄明白Obj格式定义（1小时）
1. 给Geometry类添加LoadObjFromFile()接口（1小时）
2. 添加Scene类（1小时）
3. 将Res/Geometry/tetrahedron.obj载入场景并显示（1小时）