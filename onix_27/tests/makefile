CFLAGS:= -m32 					# 32 位的程序
CFLAGS:= -Qn 					# 
# CFLAGS+= -fno-builtin			# 不需要 gcc 内置函数
# CFLAGS+= -nostdinc				# 不需要标准头文件
CFLAGS+= -fno-pic				# 不需要位置无关的代码  position independent code
#CFLAGS+= -fno-pie				# 不需要位置无关的可执行程序 position independent executable
#CFLAGS+= -nostdlib				# 不需要标准库
# CFLAGS+= -fno-stack-protector	# 不需要栈保护
CFLAGS+= -fomit-frame-pointer	# 不需要栈帧
CFLAGS+= -mpreferred-stack-boundary=3	    #不需要栈对齐
CFLAGS+= -fno-asynchronous-unwind-tables	# 不需要异常处理
CFLAGS:=$(strip ${CFLAGS})

.PHONY:hello.s
hello.s:hello.c
	gcc $(CFLAGS) -S $< -o $@

.PHONY:param.s
param.s:param.c
	gcc $(CFLAGS) -S $< -o $@

.PHONY:clean
clean:
	rm -rf *.O
	rm -rf *.out