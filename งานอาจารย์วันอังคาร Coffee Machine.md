using Microsoft.VisualBasic;
using System.Windows.Forms;

namespace WinFormsApp4
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();

            pictureBox1.MouseClick += MouseClick;
            pictureBox2.MouseClick += MouseClick;
            pictureBox3.MouseClick += MouseClick;
            pictureBox4.MouseClick += MouseClick;
        }

        private void tabPage1_Click(object sender, EventArgs e)
        {
            int price;
            string name;
            int qty;


            var clickpic = (pictureBox)sender;

            if(clickpic == pictureBox1) { 
                
                name = "Cappucino"
                    price = 20;

                qty = int.Parse(interaction.InputBox("Enter the Qty ?", "Qty",""))

                   
        }
            if (clickpic == pictureBox2)
            {
                name = "Americano"
                    price = 20;

                qty = int.Parse(interaction.InputBox("Enter the Qty ?", "Qty", ""))



        }
            if (clickpic == pictureBox3
            {

                name = "Latte"
                    price = 20;

                qty = int.Parse(interaction.InputBox("Enter the Qty ?", "Qty", ""))



        }
            if (clickpic == pictureBox4)
            {

                name = "Latte"
                    price = 20;

                qty = int.Parse(interaction.InputBox("Enter the Qty ?", "Qty", ""))



        }

            total = price * qty1;

            this.dataGridView1.Rows.Add(name, price, qty1, ToString());

            int sum = 0;

            for(int row =0; row < dataGridView1.Rows.Count; row++ )
            {
                sum = sum + Convert.ToInt32(dataGridView1Rows[row].Cells)[3].Value);
            }
       txtsum.Text = sum.ToString();




        private void pictureBox1_Click(object sender, EventArgs e)
        {

        }

        private void pictureBox3_Click(object sender, EventArgs e)
        {

        }

        private void label2_Click(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {
          
           
        }
    }
}
