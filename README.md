# cfg_def_msg

## 用途:
	* 用作通讯协议，节省网络流量，（通讯两端需提前沟通协议（配置xml文件）(配置结构体字符串)）
	* 用于运行时跟踪调试协议的，（使用界面工具配置xml文本、显示协议字段，以便交互式调试接口）

## 用法：
	* 用作通讯协议
		提前沟通好配置 (配置xml文件,结构体字符串)，后可用MsgHlp快速读取相应的字段值
	* 调试其他接口
	       通过已知协议（c++中的结构体协议），配置相应xml文件（可参考test中 .h 和 .xml）
           也可脱离xml，仅通过 结构体定义的字符串 生成解析内存机构 (需要参考 .h)
	       生成的协议 可用cvt_msg2stt(MsgInf*)显示出来，以便验证
           拿结构体字符串用MsgInf* cvt_msg2stt(string)生成内存解析结构

# 注意: 目前结构体采用紧密排列（1字节对齐，在头文件定义中使用 #pragma pack(1) #pragma pack() ）
 
