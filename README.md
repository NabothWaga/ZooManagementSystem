// Online Java Compiler
// Use this editor to write, compile and run your Java code online
//creating an animal class
class Animal {
    protected String name;
    protected int age;
//defining Animal as a public class
    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public void makeSound() {
        System.out.println("Animal is making a sound");
    }
//trying to println Animal is eating
    public void eat() {
        System.out.println("Animal is eating");
    }

    public void makeSound(int times) {
        for (int i = 0; i < times; i++) {
            makeSound();
        }
    }

    public void eat(String foodType) {
        System.out.println("Animal is eating " + foodType);
    }
}
//extended class Lion
class Lion extends Animal {
    public Lion(String name, int age) {
        super(name, age);
    }

    @Override
    public void makeSound() {
        System.out.println("Roar");
    }

    @Override
    public void eat() {
        System.out.println("Eating meat");
    }
}
//extended class Elephant 
class Elephant extends Animal {
    public Elephant(String name, int age) {
        super(name, age);
    }

    @Override
    public void makeSound() {
        System.out.println("Trumpet");
    }

    @Override
    public void eat() {
        System.out.println("Eating grass");
    }
}
//extended class Monkey
class Monkey extends Animal {
    public Monkey(String name, int age) {
        super(name, age);
    }

    @Override
    public void makeSound() {
        System.out.println("Chatter");
    }

    @Override
    public void eat() {
        System.out.println("Eating bananas");
    }
}
// class Zoo executing the functioning project
public class Zoo {
    public static void main(String[] args) {
        Animal lion = new Lion("Simba", 5);
        Animal elephant = new Elephant("Dumbo", 10);
        Animal monkey = new Monkey("Momo", 3);

        lion.makeSound();
        lion.eat();

        elephant.makeSound();
        elephant.eat();

        monkey.makeSound();
        monkey.eat();

        Animal[] animals = {lion, elephant, monkey};

        for (Animal animal : animals) {
            animal.makeSound(3);
            animal.eat("food");
        }
    }
}
