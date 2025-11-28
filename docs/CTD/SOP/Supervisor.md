# 在线管理员 标准操作流程

Supervisor standard operating procedure



## Supervisor专用扇区下载和使用

1. 进入[Github Release](https://github.com/apocfly/Supervisor-Sector-Package/releases)，进行Supervisor专用扇区下载

!!! Note
    
    此扇区不同于其他常规类型的扇区，通常不需要进行定期的更新。

2. 打开"Connection dialog"，这Callsign中**点击**“▽”，**选择**席位

    ![image-20251128235326886](./assets/image-20251128235326886.png)

3. 上线完成后，界面如下图所示：

    ![image-20251128235853193](./assets/image-20251128235853193.png)



## ".wallop" 标准处理流程

1. 这底部聊天框中查阅"SUP"频道。

    如有闪烁代表需要SUP介入帮助，此时进入"SUP"频道，查阅是哪一位用户发起的".wallop"请求，如下图：

    ![image-20251129000324386](./assets/image-20251129000324386.png)

2. 使用 `.chat XXXX_XXX` 指令，开启和这位用户的私聊

    例如：
    ```
    .chat ZBAA_APP
    ```

    !!! Warning

        严禁在SUP频道中直接回复消息
        
        !!! Note
            由于SUP频道的消息特性在: 
        	
        	SUP -> Pilot/Controller: 公共频道; 
        	
        	Pilot/Controller -> SUP频道，仅在线SUP能够查阅。

3. 依次输入：
  ```
  .hello	
  ; 填写$2的内容
  ; Hello, my name is $2, and I'm one of the Network Superivisors.
  
  ====================================================================================
  
  .how
  ; How can I help you.
  ```

4. 视情况按照 [CoC](../../General/OPDOC-General-202502-R2-SC.md) 相应条例，对涉事的管制员/机组进行处理

    ![image-20251129002053473](./assets/image-20251129002053473.png)

5. 最后，使用给予对方结束语

	```
	.close
	; The issue has been colsed.
	
	====================================================================================
	
	.enjoyp
	; Thank you very much, Enjoy your flight!
	```



## 在线检查 标准操作流程

1. 同上使用 `.chat` 指令步骤，像疑似挂机的管制员发送以下：

	```
	.res
	; Hello, Supervisor calling, please respond
	```

2. 等待约60秒，如无回复，发送第二次

	第二次隔120秒，再次不回复，发送最后30秒warning

3. 如还是未回复，使用`.kill XXXX_XXX Reasoon`移除与网络连接，例如：
	```
	.kill ZBAA_APP Do not response Supervisor message and AFK
	```
	
4. 如果回复了消息，发送结束语：
	```
	.enjoya
	; It was just a routine check if you're still behind the radar screen - thank for your time, enjoy your controllor!
	```
