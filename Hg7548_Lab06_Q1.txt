/***********************************************************************************************************************************
 * 
 * Name: Saba Begum
 * Access ID: Hg7548
 * Date: 10/19/2023
 * 
 **********************************************************************************************************************************/
package Fan;

class Fans {
	public static final int SLOW = 1;
    public static final int MEDIUM = 2;
    public static final int FAST = 3;
    
    private int _speed;
    private boolean _on;
    private double _radius;
    private String _color;

    public Fans() {
        _speed = 1;
        _on = false;
        _radius = 5;
        _color = "blue";
    }

    public Fans(int s, double r, String c, boolean onOrOff) {
        this._speed = s;
        this._radius = r;
        this._color = c;
        this._on = onOrOff;
    }

    // Accessor and mutator methods (getters and setters)...
    public int getSpeed() {
        return _speed;
    }

    public boolean isOn() {
        return _on;
    }

    public double getRadius() {
        return _radius;
    }

    public String getColor() {
        return _color;
    }

    // Mutator methods
    public void setSpeed(int speed) {
        this._speed = speed;
    }

    public void setOn(boolean on) {
        this._on = on;
    }

    public void setRadius(double radius) {
        this._radius = radius;
    }

    public void setColor(String color) {
        this._color = color;
    }
/*************************************************************************************************
 * This method will print the speed of the fan, color, and the radius if the fan is on.
 * if the fan is off then it will return the fan color and radius along with the string "fan is off"
 ***************************************************************************************************/
    public String toString() {
        if (_on) {
            return "Fan is on. Speed: " + _speed + ", Color: " + _color + ", Radius: " + _radius;
        } else {
            return "Fan is off. Color: " + _color + ", Radius: " + _radius;
        }
    }
}

public class Fan {
    public static void main(String[] args) {
        Fans fan1 = new Fans(3, 10, "yellow", true);
        Fans fan2 = new Fans(2, 5, "blue", false);

        System.out.println(fan1.toString());
        System.out.println(fan2.toString());
    }
}
