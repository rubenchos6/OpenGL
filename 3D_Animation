#include <iostream>
#include "GL/glut.h"
#include <math.h>

GLint winWidth = 600, winHeight = 600; // Initial display-window size.


/* Set coordinate limits for the clipping window: */
GLfloat xwMin = -20.0, ywMin = -20.0, xwMax = 20.0, ywMax = 20.0;

/* Set positions for near and far clipping planes: */
GLfloat dnear = 25.0, dfar = 600.0;
GLUquadricObj* quadratic;
float angle = 0;
int window_1;
float angleSphere = 0;
float xU=0, yU=0, zU=300,xC=300,yC=0,zC=300;
void drawCircle(float R, float G, float B, int radio, int x, int y, int z) {
glBegin(GL_POLYGON);
glColor3f((R / 255), (G / 255), (B / 255));
float  xf, yf;
for (float i = 0; i < 360; i += 0.5) {
xf = radio * cos(i * 3.1416 / 180);
yf = radio * sin(i * 3.1416 / 180);
glVertex3f(xf + x - 200, yf + y - 200, z);
}
glEnd();
}
void Cilindrito(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();
glTranslatef(-200 + x, 200 - y, z);
glRotatef(angle, 0, 1, 0);
quadratic = gluNewQuadric();
glColor3f((R / 255), (G / 255), (B / 255));
gluCylinder(quadratic, radio, radio, 10, 50, 50);
drawCircle(R, G, B, radio, 200, 200, 0);
drawCircle(R, G, B, radio, 200, 200, 10);

glPopMatrix();

}
void Elipcito(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();

glTranslatef(-200 + x, 200 - y, z);
glScalef(1, 2, 1); //Horizontal (2,1,1)
glRotatef(angle, 0, 1, 0);
quadratic = gluNewQuadric();
glColor3f((R / 255), (G / 255), (B / 255));
gluCylinder(quadratic, radio, radio, 10, 50, 50);
drawCircle(R, G, B, radio, 200, 200, 0);
drawCircle(R, G, B, radio, 200, 200, 10);
glPopMatrix();

}
void ElipcitoHorizontal(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();
//glRotatef(angle, 0, 1, 0);
glTranslatef(-200 + x, 200 - y, z);
glScalef(2, 1, 1);
glRotatef(angle, 0, 1, 0);
quadratic = gluNewQuadric();
glColor3f((R / 255), (G / 255), (B / 255));
gluCylinder(quadratic, radio, radio, 10, 50, 50);
drawCircle(R, G, B, radio, 200, 200, 0);
drawCircle(R, G, B, radio, 200, 200, 10);
glPopMatrix();

}
void Esferita(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();
//glRotatef(angleSphere, 0, 1, 0);
glTranslatef(-200 + x, 200 - y, z);
glRotatef(angle, 0, 1, 0);
glColor3f((R / 255), (G / 255), (B / 255));
glutSolidSphere(radio, 20, 20);
glPopMatrix();
}
void Cuadrito(float R, float G, float B, int x, int y, int z) {
glColor3f((R / 255), (G / 255), (B / 255));
glPushMatrix();
glTranslatef(-200 + x, 200 - y, z);
glScalef(.5, .5, .5);
glBegin(GL_POLYGON);
glVertex3f(0, -50, -50);
glVertex3f(0, 50, -50);
glVertex3f(50, 50, 0);
glVertex3f(50, -50, 0);
glEnd();
glBegin(GL_POLYGON);
glVertex3f(0, -50, -50);
glVertex3f(0, 50, -50);
glVertex3f(-50, 50, 0);
glVertex3f(-50, -50, 0);
glEnd();
glPopMatrix();
}
void Cuadrito2(float R, float G, float B, int x, int y, int z) {
glColor3f((R / 255), (G / 255), (B / 255));
glPushMatrix();
glTranslatef(-200 + x, 200 - y, z);
glScalef(.5, .5, .5);
glBegin(GL_POLYGON);

glVertex3f(57, 0, 0);
glVertex3f(57, 50, 0);
glVertex3f(0, 100, 0);
glVertex3f(0, 50, 0);
glEnd();
glPopMatrix();
}
void Linea(int x, int y, int z, int x2, int y2, int z2, int r, int g, int b, int line_width, int trasx, int trasy, int trasz)
{
glColor3f(r, g, b);
glPushMatrix();
glTranslatef(-200 + trasx, 200 - trasy, trasz);
glLineWidth((GLfloat)line_width);
glBegin(GL_LINES);
glVertex3i(x, y, z);
glVertex3i(x2, y2, z2);
glEnd();
glLineWidth(1.0f);
glPopMatrix();
}

void CilindritoAcostado(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();
glTranslatef(-200 + x, 200 - y, z);

glRotatef(90, 1, 0, 0);
quadratic = gluNewQuadric();
glColor3f((R / 255), (G / 255), (B / 255));
gluCylinder(quadratic, radio, radio, 10, 50, 50);
drawCircle(R, G, B, radio, 200, 200, 0);
drawCircle(R, G, B, radio, 200, 200, 10);

glPopMatrix();

}
void cuad(float R, float G, float B) {
glColor3f((R / 255), (G / 255), (B / 255));
glPushMatrix();
glTranslatef(-200 + 171, 200 - 311, 0);
glBegin(GL_POLYGON);
glVertex3f(0, -37, -37);
glVertex3f(0, 37, -37);
glVertex3f(-37, 37, 0);
glVertex3f(-37, -37, 0);
glEnd();
glPopMatrix();
}
void LineaChueca(int x, int y, int z, int x2, int y2, int z2, int r, int g, int b, int line_width, int trasx, int trasy, int trasz, int angulito)
{
glColor3f(r, g, b);
glPushMatrix();

glTranslatef(-200 + trasx, 200 - trasy, trasz);
glRotatef(-angulito, 1, 0, 0);
glLineWidth((GLfloat)line_width);
glBegin(GL_LINES);
glVertex3i(x, y, z);
glVertex3i(x2, y2, z2);
glEnd();
glLineWidth(1.0f);
glPopMatrix();
}
void Circulito3D(float R, float G, float B, int radio, int x, int y, int z) {
glPushMatrix();
glTranslatef(-200 + x, 200 - y, z);
quadratic = gluNewQuadric();
glColor3f((R / 255), (G / 255), (B / 255));
gluCylinder(quadratic, radio, radio, 5, 50, 50);
glPopMatrix();

}
void drawAll()
{

glPushMatrix();
//glRotatef(150,0,1,0);

//Cilindrito(0, 0, 255, 20, 200, 200, 0); Prueba
Cilindrito(193, 66, 47, 35, 246, 106, 0);
Cilindrito(63, 63, 65, 35, 64, 284, 0);
Cilindrito(0, 0, 0, 18, 275, 209, 0);
Esferita(0, 0, 0, 21, 320, 335, 0);
Elipcito(63, 63, 65, 18, 190, 68, 0);
Esferita(109, 46, 49, 9, 29, 60, 0); //La chirris café

ElipcitoHorizontal(0, 0, 0, 9, 169, 113, 0);

Linea(0, 120, 0, 0, -120, 0, 0, 0, 0, 2, 169, 236, 0);
Linea(0, 133, 0, 0, -133, 0, 0, 0, 0, 2, 190, 208, 0);
//Cuadrito(0, 0, 0, 0, 169, 138, 10, 169, 163, 10, 188, 181, 10, 188, 158, 10);
Cuadrito(79, 49, 17, 189, 168, 0);

Linea(0, 129, 0, 0, -129, 0, 0, 0, 0, 2, 30, 198, 0);
CilindritoAcostado(171, 141, 69, 31, 49, 347, 0);
Linea(0, 30, 0, 0, -30, 0, 0, 0, 0, 2, 49, 380, 0);
Esferita(48, 149, 107, 7, 150, 226, 0);
Esferita(145, 56, 52, 10, 269, 282, 0);
Esferita(222, 101, 108, 16, 130, 101, 0);
Cilindrito(149, 78, 36, 23, 329, 250, 0);
cuad(105, 42, 37);
glPushMatrix();
glTranslatef(50, 0, 0);
cuad(105, 42, 37);
glPopMatrix();
Elipcito(96, 70, 73, 5, 332, 113, 0);
Esferita(222, 101, 108, 8, 256, 228, 0);
Esferita(0, 0, 0, 10, 27, 336, 0);
CilindritoAcostado(0, 0, 0, 20, 29, 210, 0);
Esferita(0, 0, 0, 8, 257, 323, 0);
LineaChueca(0, 160, 0, 0, -160, 0, 0, 0, 0, 2, 100, 173, 0, 50);
Cuadrito2(198, 120, 38, 140, 204, 0);
Linea(0, 131, 0, 0, -131, 0, 0, 0, 0, 2, 332, 241, 0);
Circulito3D(0, 0, 0, 48, 252, 199, 0);
Circulito3D(0, 0, 0, 75, 170, 343, 0);
Circulito3D(0, 0, 0, 60, 133, 189, 0);


angle += .5;
angleSphere += 0.0020;

glColor4f(0, 0, .5, 0.3);
/*glBegin(GL_QUADS);
glVertex3f(-200,-200,50);
glVertex3f(-200, 200, 50);
glVertex3f(200, 200, 50);
glVertex3f(200, -200, 50);
glEnd();*/
glutSolidSphere(200, 40, 40);
//glFlush();
}
void init(void)
{

glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT);

//glColor3f(0.0, 0.0, 1.0); // Set fill color to green.
//glPolygonMode(GL_FRONT, GL_FILL);
//glPolygonMode(GL_FRONT_AND_BACK, GL_LINE); // Wire-frame back face.
//drawCircle(0, 0, 255, 20, 120, 0, 0);
//glMatrixMode(GL_MODELVIEW);
//glFrustum(xwMin, xwMax, ywMin, ywMax, dnear, dfar);
//glMatrixMode(GL_VIEWPORT);


//glLoadIdentity();
glClearColor(1.0, 1.0, 1.0, 0.0);
//glMatrixMode(GL_MODELVIEW);
//glEnable(GL_SCISSOR_TEST);
glViewport(0, 0, winWidth, winHeight/2);
glLoadIdentity();
gluLookAt(xC*sin(angleSphere), yC, zC*cos(angleSphere), 0, 0, 0, 0, 1, 0);
drawAll();
/*glMatrixMode(GL_VIEWPORT);
glViewport(0, 0, winWidth, winHeight / 2);
glScissor(0, 0, winWidth, winHeight / 2);
glLoadIdentity();
gluLookAt(0, 0, 300, 0, 0, 0, 0, 1, 0);
displayFcn();
glMatrixMode(GL_VIEWPORT);
glViewport(0, winHeight / 2, winWidth, winHeight / 2);
glScissor(0, winHeight / 2, winWidth, winHeight / 2);
glLoadIdentity();
gluLookAt(0, 0, -300, 0, 0, 0, 0, 1, 0);
displayFcn();*/
glViewport(0, winHeight/2, winWidth, winHeight / 2);
glLoadIdentity();
gluLookAt(xU, yU, zU, 0, 0, 0, 0, 1, 0);
drawAll();


//glMatrixMode(GL_PROJECTION);

////glMatrixMode();
////glFrustum(xwMin, xwMax, ywMin, ywMax, dnear, dfar);
//
//
//glEnable(GL_DEPTH_TEST);   // Enable depth testing for z-culling
//glDepthFunc(GL_LEQUAL);

//glEnable(GL_LIGHTING);
//GLfloat light1Pos[] = { -200.0,-200.0,200.0,1.0 };
//GLfloat light1Ambient[] = { 1.0,1.0,1.0,1.0 };
//GLfloat light1Diffuse[] = { 1.0,1.0,1.0,1.0 };
//GLfloat light1Specular[] = { 1.0,1.0,1.0,1.0 };
//GLfloat globalAmbient[] = { 0.0,0.0,0.3,1.0 };
//GLfloat light2Pos[] = { 200.0,200.0,200.0,1.0 };
//GLfloat light3Pos[] = { 800,800,800,1 };

//glLightfv(GL_LIGHT1, GL_POSITION, light1Pos);
//glLightfv(GL_LIGHT1, GL_AMBIENT, light1Ambient);
//glLightfv(GL_LIGHT1, GL_SPECULAR, light1Specular);

//glLightfv(GL_LIGHT2, GL_POSITION, light2Pos);
////glLightfv(GL_LIGHT2, GL_AMBIENT, light1Ambient);
//glLightfv(GL_LIGHT2, GL_DIFFUSE, light1Diffuse);
////glLightfv(GL_LIGHT2, GL_SPECULAR, light1Specular);

////glLightModelfv(GL_LIGHT_MODEL_AMBIENT,globalAmbient);
////glColorMaterial(GL_FRONT_AND_BACK,GL_COLOR_INDEXES);

//glLightfv(GL_LIGHT3, GL_POSITION, light3Pos);
////glLightfv(GL_LIGHT2, GL_AMBIENT, light1Ambient);
//glLightfv(GL_LIGHT3, GL_DIFFUSE, light1Diffuse);


//glColorMaterial(GL_FRONT, GL_AMBIENT);
//glEnable(GL_COLOR_MATERIAL);
////glCullFace(GL_BACK);

////glMaterialf(GL_FRONT, GL_SHININESS, 100.0);
////glMaterialf(GL_FRONT, GL_AMBIENT, 0.8);

//glEnable(GL_LIGHT2);
//glEnable(GL_LIGHT1);



//glEnable(GL_LINE_SMOOTH);
//glEnable(GL_POLYGON_SMOOTH);
//glHint(GL_LINE_SMOOTH_HINT, GL_NICEST);
//glHint(GL_POLYGON_SMOOTH_HINT, GL_NICEST);


//glEnable(GL_BLEND);
//glBlendFunc(GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA);

//glShadeModel(GL_SMOOTH);
//glLightModeli(GL_LIGHT_MODEL_TWO_SIDE,2);


//glDisable(GL_SCISSOR_TEST);
glutSwapBuffers();
}
float array[] = { 0,0,0,0,0,0 };//Posición, vista y color
int bandera = 0;
float pot = 0;
GLfloat luz[] = { 1,1,1,1 };
GLfloat posluz[] = { 0,0,0,1 };
void keyboard(unsigned char letra, int x, int y) {
if (bandera < 6) {
glDisable(GL_LIGHT3);
switch (letra)
{
case '1':
array[bandera] += 1 * pow(10, pot);
pot++;

break;
case '2':
array[bandera] += 2 * pow(10, pot);
pot++;
break;
case '3':
array[bandera] += 3 * pow(10, pot);
pot++;
break;
case '4':
array[bandera] += 4 * pow(10, pot);
pot++;
break;
case '5':
array[bandera] += 5 * pow(10, pot);
pot++;
break;
case '6':
array[bandera] += 6 * pow(10, pot);
pot++;
break;
case '7':
array[bandera] += 7 * pow(10, pot);
pot++;
break;
case '8':
array[bandera] += 8 * pow(10, pot);
pot++;
break;
case '9':
array[bandera] += 9 * pow(10, pot);
pot++;
break;
case '0':
pot++;
break;
case ',':
pot = 0;
bandera++;
break;
case '-':
array[bandera] = array[bandera] * (-1);
break;
default:
break;
}
}
else {
bandera = 0;
pot = 0;
printf("%f ,", array[0]);
printf("%f ,", array[1]);
printf("%f ,", array[2]);
printf("%f,", array[3]);
printf("%f ,", array[4]);
printf("%f ,", array[5]);
glLoadIdentity();
xU = array[0];
yU = array[1];
zU = array[2];

posluz[0] = array[0];
posluz[0] = array[1];
posluz[0] = array[2];
luz[0] = array[3];
luz[1] = array[4];
luz[2] = array[5];
glLightfv(GL_LIGHT3, GL_POSITION, posluz);
glLightfv(GL_LIGHT3, GL_AMBIENT, luz);
glLightfv(GL_LIGHT3, GL_DIFFUSE, luz);
glLightfv(GL_LIGHT3, GL_SPECULAR, luz);
glEnable(GL_LIGHT3);
for (int i = 0; i < 6; i++) {
array[i] = 0;
}

}
glutPostRedisplay();
}

void reshapeFcn(GLint newWidth, GLint newHeight)
{
glViewport(0, 0, newWidth, newHeight);
winWidth = newWidth;
winHeight = newHeight;

glMatrixMode(GL_PROJECTION);

//glMatrixMode();
glFrustum(xwMin, xwMax, ywMin, ywMax, dnear, dfar);


glEnable(GL_DEPTH_TEST);   // Enable depth testing for z-culling
glDepthFunc(GL_LEQUAL);

glEnable(GL_LIGHTING);
GLfloat light1Pos[] = { -200.0,-200.0,200.0,1.0 };
GLfloat light1Ambient[] = { 1.0,1.0,1.0,1.0 };
GLfloat light1Diffuse[] = { 1.0,1.0,1.0,1.0 };
GLfloat light1Specular[] = { 1.0,1.0,1.0,1.0 };
GLfloat globalAmbient[] = { 0.0,0.0,0.3,1.0 };
GLfloat light2Pos[] = { 200.0,200.0,200.0,1.0 };
GLfloat light3Pos[] = { 800,800,800,1 };

glLightfv(GL_LIGHT1, GL_POSITION, light1Pos);
glLightfv(GL_LIGHT1, GL_AMBIENT, light1Ambient);
glLightfv(GL_LIGHT1, GL_SPECULAR, light1Specular);

glLightfv(GL_LIGHT2, GL_POSITION, light2Pos);
//glLightfv(GL_LIGHT2, GL_AMBIENT, light1Ambient);
glLightfv(GL_LIGHT2, GL_DIFFUSE, light1Diffuse);
//glLightfv(GL_LIGHT2, GL_SPECULAR, light1Specular);

//glLightModelfv(GL_LIGHT_MODEL_AMBIENT,globalAmbient);
//glColorMaterial(GL_FRONT_AND_BACK,GL_COLOR_INDEXES);

glLightfv(GL_LIGHT3, GL_POSITION, light3Pos);
//glLightfv(GL_LIGHT2, GL_AMBIENT, light1Ambient);
glLightfv(GL_LIGHT3, GL_DIFFUSE, light1Diffuse);


glColorMaterial(GL_FRONT, GL_AMBIENT);
glEnable(GL_COLOR_MATERIAL);
//glCullFace(GL_BACK);

//glMaterialf(GL_FRONT, GL_SHININESS, 100.0);
//glMaterialf(GL_FRONT, GL_AMBIENT, 0.8);

glEnable(GL_LIGHT2);
glEnable(GL_LIGHT1);



glEnable(GL_LINE_SMOOTH);
glEnable(GL_POLYGON_SMOOTH);
glHint(GL_LINE_SMOOTH_HINT, GL_NICEST);
glHint(GL_POLYGON_SMOOTH_HINT, GL_NICEST);


glEnable(GL_BLEND);
glBlendFunc(GL_SRC_ALPHA, GL_ONE_MINUS_SRC_ALPHA);
glMatrixMode(GL_MODELVIEW);
}

void main(int argc, char** argv)
{
printf("Aquí aparecerán los datos que has ingresado anteriormente");
glutInit(&argc, argv);
glutInitDisplayMode(GLUT_DEPTH | GLUT_SINGLE | GLUT_RGB);
glutInitWindowPosition(0, 0);
glutInitWindowSize(winWidth, winHeight);
glutCreateWindow("PROYECTO FINAL - Perspective View of A Square");

//init();

glutDisplayFunc(init);
glutIdleFunc(init);
glutReshapeFunc(reshapeFcn);
//window_1 = glutCreateWindow(argv[0]);
//glutSetWindowTitle("Proyecto Final");
//init();
glutKeyboardFunc(keyboard);
//glutDisplayFunc(displayFcn);
//glutReshapeFunc(reshapeFcn);

glutMainLoop();
}
