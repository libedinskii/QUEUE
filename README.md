# QUEUE
Либединский Степан 2А
import java.util.LinkedList;
import java.util.NoSuchElementException;

public class Queue<T> {
    private LinkedList<T> queue = new LinkedList<T>();

    // Добавление элемента в конец очереди
    public void enqueue(T element) {
        queue.addLast(element);
    }

    // Удаление элемента из начала очереди
    public T dequeue() {
        if (queue.isEmpty()) {
            throw new NoSuchElementException("Queue is empty");
        }
        return queue.removeFirst();
    }

    // Получение элемента из начала очереди без удаления
    public T peek() {
        if (queue.isEmpty()) {
            throw new NoSuchElementException("Queue is empty");
        }
        return queue.getFirst();
    }

    // Проверка, пуста ли очередь
    public boolean isEmpty() {
        return queue.isEmpty();
    }

    // Получение размера очереди
    public int size() {
        return queue.size();
    }
}
