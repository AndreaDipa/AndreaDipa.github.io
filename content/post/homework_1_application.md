+++
title = "Homework 1, application"
date = 2022-10-03T18:34:16+02:00
draft = false
author = "Andrea Di Paolo"
+++
Assignment: 
<ul>

<li> Create simple applications in C# and VBNet to play with event handlers, understanding the syntax differences between the two languages.</li>
</ul>
<!--more-->
To practise with C# and VBNet, in particular with event handlers, I created a simple application divided into three sections. In the first part I simply make some text appear after pressing a button, in the second part I increment and decrement a progressBar again using buttons. Finally, by means of other buttons, I increment data within a histogram. <br/>
<mark>C#</mark>
```cs
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;
using System.Windows.Forms.DataVisualization.Charting;

namespace MyVeryFirstCSharpProgram
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }
        private void Form1_Load(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points.AddXY("1", 0);
            chart1.Series["Data"].Points[0].Color = Color.Red;
            chart1.Series["Data"].Points.AddXY("2", 0);
            chart1.Series["Data"].Points[1].Color = Color.Blue;
            chart1.Series["Data"].Points.AddXY("3", 0);
            chart1.Series["Data"].Points[2].Color = Color.Green;
            chart1.Series["Data"].Points.AddXY("4", 0);
            chart1.Series["Data"].Points[3].Color = Color.Purple;
        }
        private void button1_Click(object sender, EventArgs e)
        {
            richTextBox1.Text = "Hello World!";
        }

        private void button1_MouseEnter(object sender, EventArgs e)
        {
            richTextBox1.Text = "The mouse entered button1!";
        }
        private void button1_MouseLeave(object sender, EventArgs e)
        {
            richTextBox1.Text = "The mouse left button1!";

        }
        private void button2_Click(object sender, EventArgs e)
        {
            if (progressBar1.Value < 100)
            {
                progressBar1.Value += 10;
                if (progressBar1.Value == 10)
                    button3.Enabled = true;
                else if (progressBar1.Value == 100)
                    button2.Enabled = false;

            }
        }
        private void button3_Click(object sender, EventArgs e)
        {
            if (progressBar1.Value > 0)
            {
                progressBar1.Value -= 10;
                if (progressBar1.Value == 90)
                    button2.Enabled = true;
                else if (progressBar1.Value == 0)
                    button3.Enabled = false;
            }
        }

        private void button4_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[0].YValues[0] += 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }

        private void button5_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[0].YValues[0] -= 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }

        private void button6_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[1].YValues[0] += 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
        private void button7_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[1].YValues[0] -= 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
        private void button8_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[2].YValues[0] += 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
        private void button9_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[2].YValues[0] -= 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
        private void button10_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[3].YValues[0] -= 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
        private void button11_Click(object sender, EventArgs e)
        {
            chart1.Series["Data"].Points[3].YValues[0] += 1;
            chart1.ChartAreas[0].RecalculateAxesScale();
            chart1.Refresh();
        }
    }
}
```
<mark>VBNet</mark>
```vbnet
Private Sub Button1_Click(sender As Object, e As EventArgs) Handles Button1.Click
        RichTextBox1.Text = "Hello World!"
    End Sub

Private Sub Button2_Click(sender As Object, e As EventArgs) Handles Button2.Click
    If ProgressBar1.Value < 100 Then
        ProgressBar1.Value += 10

        If ProgressBar1.Value = 10 Then
            Button3.Enabled = True
        ElseIf ProgressBar1.Value = 100 Then
            Button2.Enabled = False
        End If
    End If
End Sub

Private Sub Button3_Click(sender As Object, e As EventArgs) Handles Button3.Click
    If ProgressBar1.Value > 0 Then
        ProgressBar1.Value -= 10

        If ProgressBar1.Value = 90 Then
            Button2.Enabled = True
        ElseIf ProgressBar1.Value = 0 Then
            Button3.Enabled = False
        End If
    End If
End Sub

Private Sub Button4_Click(sender As Object, e As EventArgs) Handles Button4.Click
    Chart1.Series("Data").Points(0).YValues(0) += 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button5_Click(sender As Object, e As EventArgs) Handles Button5.Click
    Chart1.Series("Data").Points(0).YValues(0) -= 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button6_Click(sender As Object, e As EventArgs) Handles Button6.Click
    Chart1.Series("Data").Points(1).YValues(0) += 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button7_Click(sender As Object, e As EventArgs) Handles Button7.Click
    Chart1.Series("Data").Points(1).YValues(0) -= 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button8_Click(sender As Object, e As EventArgs) Handles Button8.Click
    Chart1.Series("Data").Points(2).YValues(0) += 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button9_Click(sender As Object, e As EventArgs) Handles Button9.Click
    Chart1.Series("Data").Points(2).YValues(0) -= 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button10_Click(sender As Object, e As EventArgs) Handles Button10.Click
    Chart1.Series("Data").Points(3).YValues(0) += 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button11_Click(sender As Object, e As EventArgs) Handles Button11.Click
    Chart1.Series("Data").Points(3).YValues(0) -= 1
    Chart1.ChartAreas(0).RecalculateAxesScale()
    Chart1.Refresh()
End Sub

Private Sub Button1_MouseEnter(sender As Object, e As EventArgs) Handles Button1.MouseEnter
    RichTextBox1.Text = "The mouse entered button1!"
End Sub

Private Sub Button1_MouseLeave(sender As Object, e As EventArgs) Handles Button1.MouseLeave
    RichTextBox1.Text = "The mouse left button1!"
End Sub

Friend WithEvents Label1 As Label
Friend WithEvents Label2 As Label
Friend WithEvents Label3 As Label
Friend WithEvents Label4 As Label

Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
    Chart1.Series("Data").Points.AddXY("1", 0)
    Chart1.Series("Data").Points(0).Color = Color.Red
    Chart1.Series("Data").Points.AddXY("2", 0)
    Chart1.Series("Data").Points(1).Color = Color.Blue
    Chart1.Series("Data").Points.AddXY("3", 0)
    Chart1.Series("Data").Points(2).Color = Color.Green
    Chart1.Series("Data").Points.AddXY("4", 0)
    Chart1.Series("Data").Points(3).Color = Color.Purple
End Sub
```



