# BlockIconTextMenu(自定义带图标文本的块状态、条状菜单)
## 效果图<br/>
<img src="https://github.com/liuguangli/BlockIconTextMenu/blob/master/total.png" /><br/>
相信很多移动端开发者都很熟悉了，通常我们首先想到的就是使用 RelativeLayout 方式处理，例如：
<pre><code>
 &ltRelativeLayout
        android:layout_width="0dp"
        android:layout_height="fill_parent"
        android:layout_weight="1"
        android:onClick="onClickToMain"
        >
        &ltImageView
            android:layout_width="@dimen/icon_len"
            android:layout_height="@dimen/icon_len"
            android:src="@drawable/selector_icon_main"
            android:layout_centerHorizontal="true"
            android:layout_marginTop="15dp"
            />
        &ltTextView
            android:layout_width="fill_parent"
            android:layout_height="wrap_content"
            android:text="@string/index"
            android:layout_alignParentBottom="true"
            android:gravity="center"
            android:layout_marginBottom="3dp"
            android:textColor="@color/selector_common_icon_text"
            android:textSize="@dimen/common_content_text_small"
            />
    &lt/RelativeLayout>
</code></pre>
我们写一个还好，当你重复写三个以上这样的控件时你可能一直在重复复制粘贴的动作，而且你的布局层次会变得复杂而冗长。相信有追求的猿猿都会想到自定义了，于是就出现了这个开源 demo。
## 简单使用
### 1)SingleBar Style(根据需要指定右边带尖角)
效果图：<br/>
<img src="https://github.com/liuguangli/BlockIconTextMenu/blob/master/bar_single.png" /><br/>
代码：
<pre><code>
    &ltcom.blockmenu.liuguangli.blockmenuitem.BlockMenuItem
                android:layout_width="match_parent"
                android:background="@color/commonDivBgWhite"
                android:layout_marginTop="20dp"
                android:layout_height="62dp"
                app:mainIcon="@mipmap/icon_mine"
                app:IconMargin="15dp"
                app:mainIconSize="24dp"
                app:topBorder="0.5dp"
                app:bottomBorder="0.5dp"
                app:text="@string/butler"
                app:textSize="@dimen/common_content_text"
                app:textMargin="10dp"
                app:extendIcon="@mipmap/arrow_right_gray"
                />
</code></pre>
这样是不是简洁多了。
### 2）BarGroup Style
效果图：<br/>
<img src="https://github.com/liuguangli/BlockIconTextMenu/blob/master/bar_group.png" /><br/>

代码：
<pre><code>
  &ltcom.blockmenu.liuguangli.blockmenuitem.BlockMenuItem
                android:layout_width="match_parent"
                android:background="@color/commonDivBgWhite"
                android:layout_marginTop="10dp"
                android:layout_height="62dp"
                app:mainIcon="@mipmap/icon_service"
                app:IconMargin="15dp"
                app:mainIconSize="24dp"
                app:topBorder="0.5dp"
                app:bottomBorder="0.5dp"
                app:text="@string/service"
                app:textSize="@dimen/common_content_text"
                app:textMargin="10dp"
                app:extendIcon="@mipmap/arrow_right_gray"
                app:bottomBorderStartFromText="true"
                />
  &ltcom.blockmenu.liuguangli.blockmenuitem.BlockMenuItem
                android:layout_width="match_parent"
                android:background="@color/commonDivBgWhite"
                android:layout_height="62dp"
                app:mainIcon="@mipmap/icon_home"
                app:IconMargin="15dp"
                app:mainIconSize="24dp"
                app:bottomBorder="0.5dp"
                app:text="@string/shake_sopen_door"
                app:textSize="@dimen/common_content_text"
                app:textMargin="10dp"
                app:extendIcon="@mipmap/arrow_right_gray"
                />          
</code></pre>
 

 简单吧，实际上就是两个SingleBar叠在一起，然后你指定一下边界框就行了（第一个 SingleBar 的下边框指定和文本对齐，第二个  SingleBar 不设置上边框）。
 
### 3)Block Style
 效果图：<br/>
 <img src="https://github.com/liuguangli/BlockIconTextMenu/blob/master/block_simple.png" /><br/>

 代码：
<pre><code>
   &ltcom.blockmenu.liuguangli.blockmenuitem.BlockMenuItem
                        android:layout_width="fill_parent"
                        android:layout_height="fill_parent"
                        app:mainIcon="@mipmap/icon_butler_pressed"
                        app:IconMargin="15dp"
                        app:topBorder="2dp"
                        app:text="@string/butler"
                        app:textSize="@dimen/common_content_text"
                        app:textColor="@color/common"
                        app:extendIcon="@mipmap/arrow_right_gray"
                        app:textMargin="10dp"
                        app:mainIconSize="60dp"
                        app:vertical="true"
                        />
</code></pre>                       

 这个使用就更简单了，细心的你一定发现了，只需多设置一个属性：app:vertical="true"，从儿实现来图标文本的纵向排列。
 
### 4) 没有了，下载源码使用吧。
