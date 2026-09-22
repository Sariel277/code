#T1
print("Welcome to Dilidili!")
#T2
data = []
while len(data) < 7:
	data.extend(float(value) for value in input("请输入数据：").split())
#上句为ds外援 理解但还不会应用于是开始解释：.split按空白分割成多个字符串并返回一个列表，for value in ... 遍历这个列表并将每个字符串转换为浮点数，extend方法将这些浮点数添加到numbers列表中。
#ps：这个代码片段理解的逻辑顺序是什么？
if len(data) != 7:
	raise ValueError("必须输入恰好7个数据")

print(f"累计播放量为：{sum(data)}")
#T3
class User:
	def __init__(self,uname):
		self.__uname=uname #私有 封装一下
	def watch(self):
		print("观看普通视频") 
class NormalUser(User):
	def __init__(self,uname):
		super().__init__(uname)#这个应该是继承吧
class VIPUser(User):
	def watch(self):
		print("观看VIP视频")
users=[NormalUser("普通用户"), VIPUser("大会员用户")]#创建两种用户然后放进列表
for user in users:
	user.watch()#调用watch方法 多态
#T4
class Video:
	def __init__(self, title, author,views,likes):
		self.title = title
		self.author = author
		self.views = views
		self.likes = likes
def show_info(self):
    print(f"视频标题: {self.title}")
    print(f"up主: {self.author}")

    print(f"播放量: {self.views}")

    print(f"点赞数: {self.likes}")
def like(self):
    self.likes += 1
    print(f"点赞成功！")
    print(f"当前点赞数: {self.likes}")
    #读取信息数据
title=input().strip()
author=input().strip()
views=int(input().strip()) 
likes=int(input().strip())
video = Video(title, author, views, likes)
    #展示吧！视频信息！
video.show_info()
video.like()
#T5
def RC(nums,target):
	seen = {}
	#依然ds 我不是很熟练用这个于是先看例子搭了一个框架再ds启动
	for i,num in enumerate(nums):
		need=target-num
		if need in seen:
			return [seen[need],i]
		seen[num]=i
	return []
if __name__ == "__main__":
	data=input().split()
	nums=list(map(int,data[:-1]))
	target=int(input())
	result=RC(nums,target)
	print(result)
#T6
def is_palindrome(s):                                                                                                                    #这里是ds外援，意思应该是先判断再回文       
	if x<0:
		return False
	s=str(x)
	return s == s[::-1]
if __name__ == "__main__":
    x=int(input())
    result=is_palindrome(x)
    print(result)
