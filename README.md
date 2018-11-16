# Composite-ST0250-2018-2
Composite es un patrón que promueve el desarrollo de código por agrupamiento de componentes simples.

Juan Camilo Echeverri
Santiago Tello

# DD


```java
public interface Terreno {
	public void construir();
}
```


```java
public class Ladrillo implements Terreno {

	public void construir(){
		System.out.println("Colocando ladrillo");
	}
}

```


```java
public class Construccion implements Terreno {

	private ArrayList<Terreno> materiales = new ArrayList<Terreno>();

	@Override
	public void construir(){
        Terreno.construir();
	}

	public void anadir(Terreno material){
		materiales.add(material)

	}

	public void remover(Terreno material){
		materiales.remove(material);
	}
}

```



```java
public class Terrenos {

   public static void main(String[] args) {

   	  Terreno ladrillo1 = new Ladrillo();
   	  Terreno ladrillo2 = new Ladrillo();
   	  Terreno ladrillo3 = new Ladrillo();
   	  Terreno ladrillo4 = new Ladrillo();

   	  Construccion construccion = new Construccion();
   	  construccion.anadir(ladrillo1);
   	  construccion.anadir(ladrillo2);
   	  construccion.anadir(ladrillo3);
   	  construccion.anadir(ladrillo4);

   	  construccion.construir();
   	
   }

}
```
