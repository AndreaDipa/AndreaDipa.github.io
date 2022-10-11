+++
title = "Homework 2, application"
date = 2022-10-07T08:04:32+02:00
draft = false
author = "Andrea Di Paolo"
+++
Assignment:
<ul>
    <li> make a simple program which uses the objects Random and Timer </li>
    <li> Make a simple CSV parser </li>
    <li> Compute an univariate distribution of a variable</li>
</ul>
<!--more-->

# <mark> Objects Random and Timer </mark>

In order to get to grips with the two objects, I created a simple application to start the timer, so that I could randomly change the value of the progressbar, the background colour of the richtextbox and generate random passwords.

```cs
using System.Text;
using System.Windows.Forms.VisualStyles;

namespace RandomExample
{
    public partial class Form1 : Form
    {
        Random r = new Random();
        double sum = 0;
        int count = 0;
        int[] C  = new int[10];
       
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            timer1.Start();

        }
        private void timer1_Tick(object sender, EventArgs e)
        {
            double rand = r.Next(0, 100); 
            progressBar1.Value = (Int32)rand;
            richTextBox1.BackColor = Color.FromArgb(r.Next(0, 256), r.Next(0, 256), r.Next(0, 256));
            const string valid = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ1234567890";
            int length = 8;
            StringBuilder res = new StringBuilder();
            Random rnd = new Random();
            while (0 < length--)
            {
                res.Append(valid[rnd.Next(valid.Length)]);
            }
            richTextBox2.Text = res.ToString();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            timer1.Stop();
        }

        private void richTextBox1_TextChanged(object sender, EventArgs e)
        {

        }
    }
}
```
# <mark> CSV Parser and univariate distribution</mark>

```cs
using Microsoft.VisualBasic;
using Microsoft.VisualBasic.FileIO;
using System.Collections.Generic;
using System.Formats.Asn1;
using System.Windows.Forms;

namespace CSVParser
{
    public partial class Form1 : Form
    {
        string filePath = string.Empty;
        string fileContent = string.Empty;
        Stream fileStream;

        public Form1()
        {
            InitializeComponent();
           
        }
       
        private void button1_Click(object sender, EventArgs e)
        {

            if (openFileDialog1.ShowDialog() == DialogResult.OK)
            {
                filePath = openFileDialog1.FileName;
                fileStream = openFileDialog1.OpenFile();
                using (StreamReader reader = new StreamReader(fileStream))
                {
                    fileContent = reader.ReadToEnd();
                    richTextBox1.Text = fileContent;
                }


            }
            var lines = File.ReadAllLines(filePath);
            var rows = lines.Count();
            numericUpDown1.Maximum = rows;

        }

        private void openFileDialog1_FileOk(object sender, System.ComponentModel.CancelEventArgs e)
        {

        }

        private void button2_Click(object sender, EventArgs e)
        {

            dataGridView1.Rows.Clear();
            dataGridView1.Refresh();
            foreach (var headerLine in File.ReadLines(filePath).Take(1))
            {
                foreach (var headerItem in headerLine.Split(new[] { ',' }, StringSplitOptions.RemoveEmptyEntries))
                {
                    var column = new DataGridViewTextBoxColumn();
                    column.Name = headerItem;
                    column.HeaderText = headerItem;
                    dataGridView1.Columns.Add(column);
                }
            }
            var i = 0;
            
            foreach (var line in File.ReadLines(filePath).Skip(1))
            {
                 if (i < numericUpDown1.Value)
                    dataGridView1.Rows.Add(line.Split(','));
                 else
                    break;
                i++;
            }
        }
        private void dataGridView1_ColumnHeaderMouseDoubleClick_1(object sender, DataGridViewCellMouseEventArgs e)
        {
            richTextBox1.Clear();

            string[] countries = new string[((int)numericUpDown1.Value)];

            int x = 0;
            foreach (DataGridViewRow item in dataGridView1.Rows)
            {

                var ciao = item.Cells[dataGridView1.Columns[e.ColumnIndex].HeaderText].Value;

                if (ciao is not null)
                    countries[x] = ciao.ToString();
                x++;
            }


            Dictionary<string, int> times = new Dictionary<string, int>();
            foreach (var country in countries)
            {
                if (!times.ContainsKey(country))
                    times[country] = 0;
                else
                    times[country]++;

            }
            foreach (KeyValuePair<string, int> kvp in times)
            {
                richTextBox1.AppendText(kvp.Key.ToString() + " " + kvp.Value.ToString() + "\n");
            }
        }
    }
}
```

