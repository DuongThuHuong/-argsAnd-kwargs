# -argsAnd-kwargs
# Tham số dạng *args và **kwargs trong python
## ***1. *args và \**kwargs dùng để làm gì ? ***
- Khi khai báo hàm sử dụng *args và \**kwargs cho phép truyền nhiều tham số mà không cần biết trước số lượng của tham số.  
Ví dụ    
`>// giả sử tham số truyền vào đều là số  
 >def sum(*arg):  
     >total = 0  
    >for number in args:  
       >total += number  
    >return local  
  >// gọi hàm   
  >sum(1,2, 3, 19)  
  >sum(1, 100)  `  
## ***2. *args và \**kwargs khác gì nhau? ***  
- Khi gọi hàm trong python có 2 kiểu truyền tham số :  
    - Truyền tham số theo theo tên.  
    - Truyền tham số bình thường theo thứ tự khai báo đối số.  
Ví dụ  
`def register(name, password):  
 // Truyền tham số theo kiểu thông thường, phải theo đúng thứ tự  
 register('Coulson', 'hail_Hydra')  
 // Truyền tham số theo tên, không cần phải theo thứ tự khai báo tham số  
 register(password='cookHim', name='skype')  `  
 - *args nhận các tham số truyền bình thường. Sử dụng args như một list.  
 - \**kwargs nhận tham số truyền theo tên. Sử dụng kwargs như một dictionary.  
 Ví dụ  
 ` def test_args(*args):  
        for item in args:  
          print item  
   >> test_args('Hello', 'world!')  
   Hello  
   world!  
     
   def test_kwargs(**kwargs):  
      for key, value in kwargs.iteritems():  
        print('{0} = {1}'.format(key, value)  
    >> test_kwargs(name='Dzung', age=10)  
    age = 10  
    name = Dzung  `  
 ## ***3. Thứ tự sử dụng và truyền tham số *args, \**kwargs và tham số bình thường ***  
 Khi sử dụng bắt buộc phải khai báo đối số theo đúng thứ tự  
 ` *** đối số xác định --> *args --> \**kwargs ***   `
 ` *** Khi sử dụng cả *args và \**kwargs không thể truyền tham số bình thường theo tên ***   `
 Ví dụ    
 ` def show_detail(name, *args, **kwargs):  
   // gọi hàm  
    show_detail(name='Coul', 'agent', age='22')  
    >> Error  
    
   def show_detail_2(name, **kwargs):  
          
    show_detail_2(name='Coul', age='40, level='A')    
    >> chay duoc  `  
    
 
