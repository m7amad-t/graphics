
import javax.media.opengl.*;
import javax.media.opengl.awt.*;

//import com.sun.opengl.util.*;
import com.jogamp.opengl.util.Animator;

import javax.media.opengl.glu.*;

import java.awt.event.*;
import java.awt.*;

import javax.swing.*;

public class  Mohammad extends JFrame implements GLEventListener {

	GLCanvas canvas;
	Animator an;

	public Mohammad()
	{
	   super("Abdulla");
	   canvas=new GLCanvas();
	   add(canvas);
	   canvas.addGLEventListener(this);
	   an=new Animator(canvas);
	   canvas.requestFocus();
	   an.start();
	   setSize(700,600);
	   setVisible(true);
	   setLocationRelativeTo(null);
	   setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

	}

	public void init(GLAutoDrawable arg0) {
		// TODO Auto-generated method stub
		GL2 gl=arg0.getGL().getGL2();
		GLU glu=new GLU();
		gl.glClearColor(0.0f,0.0f,0.0f,0.0f);
		gl.glMatrixMode(GL2.GL_PROJECTION);
		glu.gluOrtho2D(-350, 350, -300, 300);
		gl.glMatrixMode(GL2.GL_MODELVIEW);

	}
	
	private GLAutoDrawable mainGlAutoDrawable;
	
	public void convertTo255RGB(int r, int g, int b) {
		float rColor = (float)r / 255;
	    float gColor = (float)g / 255;
	    float bColor = (float)b / 255;
	     
	    GL2 gl=mainGlAutoDrawable.getGL().getGL2();
	    
	    gl.glColor3f(rColor, gColor, bColor);
	}

	
	public void display(GLAutoDrawable arg0) {
		mainGlAutoDrawable = arg0;
		// TODO Auto-generated method stub
		GL2 gl=arg0.getGL().getGL2();
		gl.glClear(GL2.GL_COLOR_BUFFER_BIT);
		gl.glLineWidth(3);
		
		convertTo255RGB(229, 204, 153);
	    
	    gl.glPolygonMode(GL2.GL_FRONT, GL2.GL_LINE);
	    gl.glPolygonMode(GL2.GL_BACK, GL2.GL_FILL);
	   
	    gl.glFrontFace(GL2.GL_CW);
	   
	    
	    //Bottom Square
	    gl.glBegin(GL2.GL_POLYGON);
	    
	    gl.glVertex2i(0, -100);
	    gl.glVertex2i(0, -60);
	    gl.glVertex2i(-250, -60);
	    gl.glVertex2i(-250, -100);
	  
	    gl.glEnd();
	    
	    
	    //Left half polygon
	    gl.glBegin(GL2.GL_POLYGON);
	    
	    gl.glVertex2i(-180, -60);
	    gl.glVertex2i(-180, 50);
	    //Nuki lay chapy xanwaka 
	    gl.glVertex2i(-205, 75);
	    gl.glVertex2i(-230, 50);
	    gl.glVertex2i(-230, -60);
	    
	    gl.glEnd();
	    
	    gl.glBegin(GL2.GL_POLYGON);
	
	    gl.glVertex2i(-180, 85);
	    gl.glVertex2i(-180, -60);
	    gl.glVertex2i(-40, -60);
	    gl.glVertex2i(-40, 85);
	    //Nuki lay rasty xanwaka
	    gl.glVertex2i(-110, 110);
	    /////
	    gl.glVertex2i(-180, 85);
	    gl.glEnd();
	    
	    //House Door
	    convertTo255RGB(127, 51, 28);
	    gl.glBegin(GL2.GL_POLYGON);
	    
	    gl.glVertex2i(-110, -100);
	    gl.glVertex2i(-110, -20);
	    gl.glVertex2i(-140, -20);
	    gl.glVertex2i(-140, -100);
	    
	    gl.glEnd();
	    
	    //Window
	    convertTo255RGB(255, 196, 28);
	    gl.glPointSize(35f);
	    gl.glBegin(GL2.GL_POINTS);
	    
	    gl.glVertex2i(-85, 25);
	    
	    gl.glEnd();	    
	    
	    //Door Lock
	    gl.glPointSize(10f);
	    gl.glBegin(GL2.GL_POINTS);
	    gl.glVertex2i(-120, -60);
	    gl.glEnd();
	    
	    parzhin(arg0);
	    
	    road(arg0);
	}
	
	public void parzhin(GLAutoDrawable arg0) {
		GL2 gl=arg0.getGL().getGL2();
		
		convertTo255RGB(166, 122, 43);
		gl.glLineWidth(4f);
		
		gl.glBegin(GL2.GL_LINES);
		for (int i = -345; i < 350; i+= 9) {
		    
		    gl.glVertex2i(i, -110);
		    gl.glVertex2i(i, -85);
		    
		}
		
		gl.glVertex2i(-350, -102);
	    gl.glVertex2i(350, -102);
	    gl.glEnd();
	    
	}

	public void road(GLAutoDrawable arg0) {
		GL2 gl=arg0.getGL().getGL2();
		
		convertTo255RGB(127, 127, 127);
	    gl.glBegin(GL2.GL_POLYGON);
	    
	    gl.glVertex2i(-350, -110);
	    gl.glVertex2i(-350, -170);
	    gl.glVertex2i(350, -170);
	    gl.glVertex2i(350, -110);
	    gl.glEnd();
	    
	    
	    //Middle white line of the road
	    gl.glColor3f(1, 1, 1);
	    gl.glLineWidth(3);
		gl.glEnable(GL2.GL_LINE_STIPPLE);
		gl.glEnable(GL2.GL_LINE_SMOOTH);
		gl.glLineStipple(1,(short)0xFF00);
		gl.glBegin(GL2.GL_LINES);
	    gl.glVertex2i(-350, -140);
	    gl.glVertex2i(350, -140);
	    
	    gl.glEnd();
	    gl.glDisable(GL2.GL_LINE_STIPPLE);
	}
	public void dispose(GLAutoDrawable arg0) {
		// TODO Auto-generated method stub

	}

	public void reshape(GLAutoDrawable arg0, int arg1, int arg2, int arg3,
			int arg4) {
		// TODO Auto-generated method stub

	}

	public static void main(String[] arg)
	{
		new abdulla();
	}

}
