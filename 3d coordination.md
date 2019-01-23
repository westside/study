## 3d 그래픽 하다보면 항상 헷갈려서 정리

### homogeneous 좌표(잊지말자)
* (x, y, z)의 3차원좌표에 w를 더한거다. 그래서 (x, y, z, w)
```
w 가 1이면 vector (x, y, z, 1) 는 위치(position)다.
w 가 0이면 vector (x, y, z, 0) 은 방향(direction)이다.
```

* 왜 이렇게 하는걸까? 이렇게 하면 하나의 식으로 translation(물체의 좌표 이동) 이랑 rotation(물체의 회전) 두개를 다 다룰 수 있기 때문이다. 
* 예를 들어서 translate은 (10, 10, 10, 1) vector를 x축으로 10만큼 translate하려면 (10, 0, 0, 1)을 쓰면 된다. 

![img](http://www.opengl-tutorial.org/assets/images/tuto-3-matrix/translationExamplePosition1.png)

* 반면에 (0, 0, -1, 0) vector에 대해서 translation을 더한다고 해도 그 값은 바뀌지 않는다. rotation이니까

![img](http://www.opengl-tutorial.org/assets/images/tuto-3-matrix/translationExampleDirection1.png)


### Transform Matrix
* 우선 4X4 Matrix를 많이 쓰는데 그 이유는 4차원 vertex를 곱해서 transform 하기 위해서다. 

Matrix X Vertex = TransformedVertex

![img](http://www.opengl-tutorial.org/assets/images/tuto-3-matrix/MatrixXVect.gif)



### Euler angle, Quatenion
* 오일러 앵글이 실제 보기에는 쉽고 (yaw, pitch, roll) 
* 쿼터니언이 계산하기 쉽다
* 즉 내부적으론 쿼터니언으로 쓰고 외부에는 오일러로 쓸수 있게 하면 된다. 


## 참조
* http://www.opengl-tutorial.org/beginners-tutorials/tutorial-3-matrices/
* http://www.songho.ca/opengl/gl_matrix.html
* rotation 관련 
