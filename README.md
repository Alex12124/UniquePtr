# UniquePtr

Напишите свою упрощённую реализацию класса unique_ptr<T>. В этой задаче вам не нужно делать специализацию для массива и не нужно предусматривать свой Deleter. Назовите ваш класс UniquePtr. У класса должен быть один шаблонный параметр T — тип элемента, указатель на который будет храниться внутри.

Напишите следующие функции в классе:

  1.  Конструктор по умолчанию, создающий пустой умный указатель.

  2.  Конструктор, принимающий T* и захватывающий владение этой динамической памятью.

  3.  Конструктор перемещения, получающий на вход rvalue-ссылку на другой UniquePtr и отбирающий у него владение ресурсом.

  4.  Оператор присваивания, получающий на вход nullptr (тип - nullptr_t, определенный в заголовочном файле cstddef). В результате умный указатель должен стать пустым.

  5.  Move-оператор присваивания, получающий на вход rvalue-ссылку на другой UniquePtr.

  6.  Деструктор.

  7.  operator *, который возвращает T&.

  8.  Оператор -> (он должен вернуть указатель на обычную структуру, к которому можно применить обычный ->).

  9.  Функцию T* Release(), отменяющую владение объектом и возвращающую хранящийся внутри указатель.

  10.  Функцию void Reset(T* ptr), после выполнения которой умный указатель должен захватить ptr.

  11.  Функцию void Swap(UniquePtr& other), обменивающуюся содержимым с другим умным указателем.

  12.  Функцию T* Get() const, возвращающую указатель.

В вашем классе должны быть запрещены конструктор копирования и обычный оператор присваивания.

Использовать стандартный unique_ptr и заголовочный файл memory запрещается.
