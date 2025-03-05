public class Task {
ArrayList<String> Task = new ArrayList<>();

public void addTask(String description, int priority, int minutes) {
    if (priority > 4 || priority < 1) {
        System.out.println(description + " has invalid priority ");
    }
    if (minutes < 0) {
        System.out.println(description + " has invalid workload ");
    }
    Todo.add(Task.class.getName());
}

public void getTodoList() {
    Todo.forEach(item->System.out.println(Task.class.getName().toString()));
}

public void print() {
    System.out.println("Todo:");
    System.out.println("-----");
    getTodoList();
    if (Todo == null) {
        System.out.println("You're all done for today! #TodoZero");
    }
}

public static void main(String[] args) {
    Task task;
    Todo todo;
    todo = new Todo();
    todo.addTask("Go to gym", 2, 60);
    todo.addTask("Read book", 1, 45);
    todo.print();
    System.out.print("");
}
}

