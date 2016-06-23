Laravel的event功能提供一个简单的观察者实现，允许你在应用程序里订阅与监听事件。事件类通常被保存在 app/Events 目录下，而它们的处理程序则被保存在 app/Handlers/Events 目录下。

1.订阅事件
  laravel里的EventServiceProvider提供一个方便的地方注册所有的事件处理程序。
  
2.触发事件
  使用Event Facade触发我们的事件：
  $response = Event::fire(new PodcastWasPurchased($podcast));
fire 方法返回一个响应的数组，让你可以用来控制你的应用程序接下来要有什么反应。