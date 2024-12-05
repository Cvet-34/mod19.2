<h3 align="center">Домашнее работа QuerySet. </h3>
<p>переходим в специальнаую консоль:</p>
<p>python manage.py shell</p>
<p>далее вводим QuerySet запросы:</p>
<p>импортируем модель Buyer:</p>
<p>from task1.models import Buyer</p>
<p>создаем объекты для таблицы Buyer</p>
<p>Buyer.objects.create(id=2, name ='Ilya', balance=1500.05, age=24)</p>
<p>Buyer.objects.create(id=3, name ='Terminator2000', balance=42.15, age=52)</p>
<p>Buyer.objects.create(id=4, name ='Ubvator432', balance=0.5, age=16)</p>
<p>импортируем модель Game:</p>
<p>from task1.models import Game</p>
<p>создаем объекты для таблицы Game:</p>
<p>Game.objects.create(id=2, title='Cyberpunk', cost=31, size=46.2, description='Game of the year', age_limited=1)</p>
<p>Game.objects.create(id=3, title='Mario', cost=5, size=0.5, description='Old Game', age_limited=0)</p>
<p>Game.objects.create(id=4, title='Hitman', cost=12, size=36.6, description='Who', age_limited=1)
Game свяжите их полем buyer: 
Game.objects.get(id=2).buyer.set((2, 3))
Game.objects.get(id=4).buyer.set((2, 3))
Game.objects.get(id=3).buyer.set((2, 3, 4))</p>
exit() завершаем работу выходим из спец консоли.
