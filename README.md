<h3 align="center">Домашняя работа QuerySet запросы. </h3>
<h4>Переходим в специальнаую консоль:</h4>
<p>python manage.py shell</p>
<h4> Далее вводим QuerySet запросы:</h4>
<p>1. импортируем модель Buyer:</p>
<p>from task1.models import Buyer</p>
<p>2. создаем объекты для таблицы Buyer:</p>
<p>Buyer.objects.create(id=2, name ='Ilya', balance=1500.05, age=24)</p>
<p>Buyer.objects.create(id=3, name ='Terminator2000', balance=42.15, age=52)</p>
<p>Buyer.objects.create(id=4, name ='Ubvator432', balance=0.5, age=16)</p>
<p>3. импортируем модель Game:</p>
<p>from task1.models import Game</p>
<p>4. создаем объекты для таблицы Game:</p>
<p>Game.objects.create(id=2, title='Cyberpunk', cost=31, size=46.2, description='Game of the year', age_limited=1)</p>
<p>Game.objects.create(id=3, title='Mario', cost=5, size=0.5, description='Old Game', age_limited=0)</p>
<p>Game.objects.create(id=4, title='Hitman', cost=12, size=36.6, description='Who', age_limited=1)</p>
<p>5. Game связываем с полем buyer:</p> 
<p>Game.objects.get(id=2).buyer.set((2, 3))</p>
<p>Game.objects.get(id=4).buyer.set((2, 3))</p>
<p>Game.objects.get(id=3).buyer.set((2, 3, 4))</p>
<p>6. exit() завершаем работу выходим из спец консоли.</p>
