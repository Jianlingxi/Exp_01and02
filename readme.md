* [Helloworld](#Helloworld)
######  简单布局
* [1.主页](#主页)
* [2.表格布局](#表格布局)
* [3.线性布局](#线性布局)
* [4.计算器布局](#计算器布局)
######  约束布局
* [约束布局](#约束布局)



## Helloworld
#### 利用了Android Studio 布局编辑器创建了简易界面，体验了一下Android Studio
![HelloWorld](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/helloworld.png?raw=true)
**********************************

## 主页
### 创建三个按钮分别进入表格布局、线性布局和计算器布局
#### 代码
        <Button
            android:id="@+id/button_one"
            android:layout_width="120dp"
            android:layout_height="wrap_content"
            android:background="@color/white"
            android:text="表格布局"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintLeft_toLeftOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            tools:ignore="MissingConstraints"></Button>

        <Button
            android:id="@+id/button_two"
            android:layout_width="120dp"
            android:layout_height="wrap_content"
            android:layout_marginLeft="144dp"
            android:background="@color/white"
            android:text="线性布局"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintLeft_toLeftOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            tools:ignore="MissingConstraints"></Button>

        <Button
            android:id="@+id/button_three"
            android:layout_width="120dp"
            android:layout_height="wrap_content"
            android:background="@color/white"
            android:text="计算器布局"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintRight_toRightOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            tools:ignore="MissingConstraints"></Button>
#### JAVA代码
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button btn = findViewById(R.id.button_one);
        Button btn1 = findViewById(R.id.button_two);
        Button btn2 = findViewById(R.id.button_three);
        btn.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View view){
                Intent intent = new Intent(MainActivity.this,layout_1.class);
                startActivity(intent);
            }
        });
        btn1.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View view){
                Intent intent = new Intent(MainActivity.this,layout_2.class);
                startActivity(intent);
            }
        });
        btn2.setOnClickListener(new View.OnClickListener(){
            @Override
            public void onClick(View view){
                Intent intent = new Intent(MainActivity.this,layout_3.class);
                startActivity(intent);
            }
        });
#### 效果展示
![主页](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/index.png?raw=true)
**************************************

## 表格布局
#### 代码

        <TableRow
            android:background="#8B8989"
            >
            <TextView
                android:text="Hello TableLayout"
                android:paddingLeft="5dp"
                android:textSize="20dp"
                android:textColor="#fff"
                android:textFontWeight="3"></TextView>
        </TableRow>
        <TableRow
            android:background="#000"
            >
            <TextView
                android:text="Open...."
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
            <TextView
                android:text="Ctrl+O"
                android:gravity="right"
                android:textColor="#fff"
                android:paddingRight="10dp"/>
        </TableRow>
        <TableRow
            android:background="#000"
            >
            <TextView
                android:text="Save...."
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
            <TextView
                android:text="Ctrl+S"
                android:textColor="#fff"
                android:gravity="right"
                android:paddingRight="10dp"/>
        </TableRow>
        <TableRow
            android:background="#000">
            <TextView
                android:text="Save as...."
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
            <TextView
                android:text="Ctrl+Shift+S"
                android:gravity="right"
                android:textColor="#fff"
                android:paddingRight="10dp"/>
        </TableRow>
        <TableRow
            android:background="#000">
            <TextView
                android:text="X Import...."
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
        </TableRow>
        <TableRow
            android:background="#000">
            <TextView
                android:text="X Export...."
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
            <TextView
                android:text="Ctrl+E"
                android:textColor="#fff"
                android:gravity="right"
                android:paddingRight="10dp"/>
        </TableRow>
        <TableRow
            android:background="#000">
            <TextView
                android:text="  Quit"
                android:textColor="#fff"
                android:paddingLeft="10dp"/>
        </TableRow>
#### 效果展示
![表格布局](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/table.png?raw=true)
*********************************************
## 线性布局
#### 部分代码
        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="50dp"
            android:orientation="horizontal"
            >


            <TextView
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_weight="1"
                android:text="One,One"
                android:background="@Exp_01and02able/setbar_bg"
                android:textColor="#fff"
                android:textSize="12dp"
                android:gravity="center"
                />
            <TextView
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_weight="1.3"
                android:layout_marginLeft="3dp"
                android:text="One,Two"
                android:background="@Exp_01and02able/setbar_bg"
                android:textColor="#fff"
                android:textSize="12dp"
                android:gravity="center"/>
            <TextView
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_marginLeft="3dp"
                android:layout_weight="1"
                android:text="One,Three"
                android:background="@Exp_01and02able/setbar_bg"
                android:textColor="#fff"
                android:textSize="12dp"
                android:gravity="center"/>
            <TextView
                android:layout_width="0dp"
                android:layout_height="50dp"
                android:layout_weight="1"
                android:layout_marginLeft="3dp"
                android:text="One,Four"
                android:background="@Exp_01and02able/setbar_bg"
                android:textColor="#fff"
                android:textSize="12dp"
                android:gravity="center"/>
        </LinearLayout>
#### 效果展示
![线性布局](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/linear.png?raw=true)
*********************************************
## 计算器布局
#### 部分代码
        <TextView   
            android:layout_margin="10dp"
            android:layout_width="match_parent"
            android:paddingLeft="10dp"
            android:textColor="#A9A9A9"
            android:layout_height="40dp"
            android:textSize="30dp"
            android:text="Input"
            />
        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_margin="10dp"
            android:gravity="right"
            android:textSize="25dp"
            android:paddingRight="5dp"
            android:background="#BBBB99"
            android:text="0.0"
            >
        </TextView>
        <LinearLayout
            android:layout_marginTop="50dp"
            android:layout_marginLeft="10dp"
            android:layout_marginRight="10dp"
            android:layout_width="match_parent"
            android:layout_height="60dp"

            android:orientation="horizontal">
            <Button
                android:id="@+id/Number7"
                android:layout_width="70dp"
                android:layout_height="wrap_content"
                android:text="7"
                android:textSize="20dp"
                android:layout_weight="5"
                ></Button>
            <Button
                android:id="@+id/Number8"
                android:layout_width="70dp"
                android:layout_height="wrap_content"
                android:layout_marginLeft="35dp"
                android:text="8"
                android:textSize="20dp"
                android:layout_weight="5"
                ></Button>
            <Button
                android:id="@+id/Number9"
                android:layout_width="70dp"
                android:layout_height="wrap_content"
                android:layout_marginLeft="35dp"
                android:text="9"
                android:textSize="20dp"
                android:layout_weight="5"
                ></Button>
            <Button
                android:id="@+id/chuhao"
                android:layout_width="70dp"
                android:layout_height="wrap_content"
                android:layout_marginLeft="35dp"
                android:text="÷"
                android:textSize="20dp"
                android:layout_weight="5"
                ></Button>
        </LinearLayout>
#### 效果展示
![计算器布局](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/calculator.png?raw=true)
*********************************************

## 约束布局
#### 部分代码
        <ImageView
            android:id="@+id/spaceStationIcon"
            android:layout_width="30dp"
            android:layout_height="30dp"
            android:layout_marginTop="15dp"
            android:src="@Exp_01and02able/space_station_icon"
            app:layout_constraintEnd_toStartOf="@+id/flightsIcon"
            app:layout_constraintHorizontal_chainStyle="spread"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent" />

        <ImageView
            android:id="@+id/flightsIcon"
            android:layout_width="30dp"
            android:layout_height="30dp"
            android:src="@Exp_01and02able/rocket_icon"
            app:layout_constraintBottom_toBottomOf="@+id/spaceStationIcon"
            app:layout_constraintEnd_toStartOf="@+id/roverIcon"
            app:layout_constraintStart_toEndOf="@+id/spaceStationIcon"
            app:layout_constraintTop_toTopOf="@+id/spaceStationIcon" />

        <ImageView
            android:id="@+id/roverIcon"
            android:layout_width="30dp"
            android:layout_height="30dp"
            android:src="@Exp_01and02able/rover_icon"
            app:layout_constraintBottom_toBottomOf="@+id/flightsIcon"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toEndOf="@+id/flightsIcon"
            app:layout_constraintTop_toTopOf="@+id/flightsIcon" />

        <TextView
            android:id="@+id/roverLabel"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="15dp"
            android:text="@string/rovers"
            app:layout_constraintEnd_toEndOf="@+id/roverIcon"
            app:layout_constraintStart_toStartOf="@+id/roverIcon"
            app:layout_constraintTop_toBottomOf="@+id/roverIcon" />

        <TextView
            android:id="@+id/flightsLabel"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="15dp"
            android:text="@string/flights"
            app:layout_constraintEnd_toEndOf="@+id/flightsIcon"
            app:layout_constraintStart_toStartOf="@+id/flightsIcon"
            app:layout_constraintTop_toBottomOf="@+id/flightsIcon" />

        <TextView
            android:id="@+id/spaceStationLabel"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginTop="15dp"
            android:text="@string/space_stations"
            app:layout_constraintEnd_toEndOf="@+id/spaceStationIcon"
            app:layout_constraintStart_toStartOf="@+id/spaceStationIcon"
            app:layout_constraintTop_toBottomOf="@+id/spaceStationIcon" />

        <TextView
            android:id="@+id/textView1"
            android:layout_width="124dp"
            android:layout_height="98dp"
            android:layout_centerVertical="true"
            android:layout_marginEnd="44dp"
            android:layout_toStartOf="@id/doubleArrowsIcon"
            android:background="@color/colorPrimary"
            android:gravity="center"
            android:paddingEnd="20dp"
            android:text="@string/dca"
            android:textColor="@android:color/white"
            app:layout_constraintBottom_toBottomOf="@+id/doubleArrowsIcon"
            app:layout_constraintEnd_toEndOf="@+id/doubleArrowsIcon"
            app:layout_constraintTop_toTopOf="@+id/doubleArrowsIcon" />

        <TextView
            android:id="@+id/textView2"
            android:layout_width="124dp"
            android:layout_height="98dp"
            android:layout_centerVertical="true"
            android:layout_marginStart="44dp"
            android:layout_toEndOf="@id/doubleArrowsIcon"
            android:background="@color/colorPrimary"
            android:gravity="center"
            android:paddingStart="20dp"
            android:text="@string/mars"
            android:textColor="@android:color/white"
            app:layout_constraintBottom_toBottomOf="@+id/doubleArrowsIcon"
            app:layout_constraintStart_toStartOf="@+id/doubleArrowsIcon"
            app:layout_constraintTop_toTopOf="@+id/doubleArrowsIcon" />

        <ImageView
            android:id="@+id/doubleArrowsIcon"
            android:layout_width="60dp"
            android:layout_height="60dp"
            android:layout_centerInParent="true"
            android:layout_marginBottom="40dp"
            android:src="@Exp_01and02able/double_arrows"
            app:layout_constraintBottom_toTopOf="@+id/guideline1"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent" />

        <android.support.constraint.Guideline
            android:id="@+id/guideline1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            app:layout_constraintGuide_begin="200dp" />

        <android.support.constraint.Guideline
            android:id="@+id/guideline2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:orientation="vertical"
            app:layout_constraintGuide_percent=".05" />

        <Switch
            android:id="@+id/switch1"
            android:layout_width="160dp"
            android:layout_height="wrap_content"
            android:layout_marginStart="8dp"
            android:layout_marginTop="200dp"
            android:background="@color/colorAccent"
            android:padding="8dp"
            android:switchPadding="24dp"
            android:text="@string/one_way"
            android:textColor="@android:color/white"
            app:layout_constraintStart_toStartOf="@+id/guideline2"
            app:layout_constraintTop_toTopOf="parent" />

        <TextView
            android:id="@+id/textView3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_below="@id/switch1"
            android:layout_marginStart="8dp"
            android:layout_marginTop="8dp"
            android:background="@color/colorAccent"
            android:padding="8dp"
            android:text="@string/traveller"
            android:textColor="@android:color/white"
            app:layout_constraintStart_toStartOf="@+id/guideline2"
            app:layout_constraintTop_toBottomOf="@+id/switch1" />

        <ImageView
            android:id="@+id/rocketIcon"
            android:layout_width="30dp"
            android:layout_height="30dp"
            android:src="@Exp_01and02able/rocket_icon"
            app:layout_constraintCircle="@id/galaxyIcon"
            app:layout_constraintCircleAngle="270"
            app:layout_constraintCircleRadius="100dp" />

        <ImageView
            android:id="@+id/galaxyIcon"
            android:layout_width="90dp"
            android:layout_height="90dp"
            android:layout_centerInParent="true"
            android:layout_marginTop="8dp"
            android:layout_marginBottom="8dp"
            android:src="@Exp_01and02able/galaxy"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintHorizontal_bias="0.5"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="@+id/guideline1" />

        <Button
            android:id="@+id/departButton"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginBottom="8dp"
            android:text="@string/depart"
            android:textColor="@android:color/white"
            app:backgroundTint="@color/colorPrimary"
            app:layout_constraintBottom_toBottomOf="parent" />

        </android.support.constraint.ConstraintLayout>
#### 效果展示
![约束布局](https://github.com/Jianlingxi/Exp_01and02/blob/master/DRAW/ring.png?raw=true)
*********************************************


