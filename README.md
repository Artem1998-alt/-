package ru.mirea.gib04.lab7;

import java.util.*;

public class AbstractListDemo {
    public static void main(String args[])
    {

        // Creating an empty AbstractList
        AbstractList<String>
                list = new LinkedList<String>();

        // Using add() method to add elements in the list
        list.add("children");
        list.add("for");
        list.add("children");
        list.add("20");
        list.add("30");

        // Output the list
        System.out.println("AbstractList: " + list);

        // Remove the head using remove()
        list.remove(3);

        // Print the final list
        System.out.println("Final AbstractList: " + list);

        // getting the index of last occurence
        // using lastIndexOf() method
        int lastindex = list.lastIndexOf("A");

        // printing the Index
        System.out.println("Last index of A : "
                + lastindex);
    }
} 

package ru.mirea.gib04.lab7;

import java.util.ArrayList;

public class CollectionApp {

    public static void main(String[] args) {

        ArrayList<String> states = new ArrayList<String>();
        // добавим в список ряд элементов
        states.add("Россия");
        states.add("Польша");
        states.add("Англия");
        states.add("США");
        states.add(1, "Франция"); // добавляем элемент по индексу 1

        System.out.println(states.get(1));// получаем 2-й объект
        states.set(1, "Уганда"); // установка нового значения для 2-го объекта

        System.out.printf("В списке %d элементов \n", states.size());
        for(String state : states){

            System.out.println(state);
        }

        if(states.contains("Россия")){

            System.out.println("Список содержит государство Россия");
        }

        // удалим несколько объектов
        states.remove("Россия");
        states.remove(0);

        Object[] countries = states.toArray();
        for(Object country : countries){

            System.out.println(country);
        }
    }
} 

package ru.mirea.gib04.lab7;

import java.util.LinkedList;

public class KollectionApp {

    public static void main(String[] args) {

        LinkedList<String> states = new LinkedList<String>();

        // добавим в список ряд элементов
        states.add("Россия");
        states.add("Польша");
        states.addLast("Англия"); // добавляем на последнее место
        states.addFirst("США"); // добавляем на первое место
        states.add(1, "Франция"); // добавляем элемент по индексу 1

        System.out.printf("В списке %d элементов \n", states.size());
        System.out.println(states.get(1));
        states.set(1, "Уганда");
        for(String state : states){

            System.out.println(state);
        }
        // проверка на наличие элемента в списке
        if(states.contains("Россия")){

            System.out.println("Список содержит государство Россия");
        }

        states.remove("Россия");
        states.removeFirst(); // удаление первого элемента
        states.removeLast(); // удаление последнего элемента

        LinkedList<Person> people = new LinkedList<Person>();
        people.add(new Person("Masha"));
        people.addFirst(new Person("Petor"));
        people.addLast(new Person("ALeks"));
        people.remove(1); // удаление второго элемента

        for(Person p : people){

            System.out.println(p.getName());
        }
        Person first = people.getFirst();
        System.out.println(first.getName()); // вывод первого элемента
    }
}
class Person{

    private String name;
    public Person(String value){

        name=value;
    }
    String getName(){return name;}
} 
