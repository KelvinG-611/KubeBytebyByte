# Day 1

## Topic 1. Virtualization vs. Minikube

**Minikube** utilizes **virtualization** to run a lightweight Kubernetes cluster on a local machine, simulating a full-fledged Kubernetes environment within a single virtual machine.

Q1: What is virtualization technology?

Imagine you have a spacious open-plan apartment with no separate rooms. This room is where you do all your activities - work, play, and rest. Now, suppose you want to have separate dedicated spaces for certain activities, like an office for working or a playroom for games. However, you can't afford to buy a new apartment. The best way to achieve this is by hiring a contractor to partition off new rooms.

In the tech world, the spacious apartment represents your computer, more specifically your operating system, such as MacOS or Windows. Your daily activities - work, play, and rest - are the programs running on your computer. The contractor that knows how to separate rooms is called virtualization technology. The new rooms, like the work office and playroom, are referred to as virtual machines.

So if you're using virtualization:

- Your one computer can pretend to be many computers.
- Each "pretend" computer can run a different operating system, like Windows in one and Linux in another.
- You can run different programs or tasks in these separate systems without them affecting each other. For example, developers use virtualization to test software on different operating systems without needing several separate physical computers. Or, you can use it to run a program that only works on Windows while you're using a Mac, by running a virtual Windows computer on your Mac.

Q2: What is Minikube? Why do we use minikube?


# Topic 2. Pod 
1. What is Pod?

Imagine Pod as a shared department where each room is a container. ![image](https://github.com/KelvinG-LGTM/KubeBytebyByte/assets/13389755/d73d8a3a-bc05-4850-a3d9-40c03426b909)

2. Analog to describe the relationship between pod and containers
   Imagine a fast-food company founded by a team of three friends. They decided to operate their business from a food truck. Each friend has a specific role: one handles cash transactions, another is responsible for cooking, and the third prepares ingredients. They all share common facilities within the truck like the washroom, kitchen, and fridge. If they need to replace any equpiment or decide to operate from a different truck, they simply lease another one and run their business there.

   In this analogy, the fast food company is akin to a pod. The food truck is analogous to a node, providing the necessary infrastructure and environment for the company (the pod) to function. The three friends represents the containers in the pod, each performing a distinct task but sharing common resources and infrastructure. Just as the friends share the facilities of the truck, containers in a pod share common resources like the local network and mounted volumes.
   
4. What's the design philosophy of using Pod?
   Team work. How do we achieve goal with shared resources.
   

## Others
1. What Github Gist?

  Notepad for your code and text that can easily share with others.

2. What is `__setitem()` method?
`__setitem()` is a special method in python that allows you to set the value of the item in an object using **square bracket notation**.
```python
class Test:
  def __init__(self):
    self.dic = {}

  def __setitem__(self, key, value):
    self.dic[key] = value

if __name__ == "__main__":
  test_instance = Test()
  test_instance["key1"] = "value1" # This will call __setitem__ method
```
