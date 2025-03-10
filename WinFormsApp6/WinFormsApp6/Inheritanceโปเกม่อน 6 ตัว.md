using System.Windows.Forms;

namespace WinFormsApp6
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void comboBox1_SelectedIndexChanged(object sender, EventArgs e)
        {
            
            string imagePath = "\"E:\\Pokemon\\025.png\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Pikachu";
            maskedTextBox2.Text = "Electric";
            maskedTextBox3.Text = "Active";
        }

        private void comboBox7_SelectedIndexChanged(object sender, EventArgs e)
        {

        }

        private void comboBox9_SelectedIndexChanged(object sender, EventArgs e)
        {
            private void btnCharizard_Click(object sender, EventArgs e)
        {
            
            string imagePath = "\"E:\\Pokemon\\Pok?mon_Charizard_art.png\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Charizard";
            maskedTextBox2.Text = "\"Fire/Flying\";";
            maskedTextBox3.Text = "Active";
        }

        private void btnBulbasaur_Click(object sender, EventArgs e)
        {
          
            string imagePath = "\"E:\\Pokemon\\images.jpg\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Groudon";
            maskedTextBox2.Text = "\"Ground\"; ";
            maskedTextBox3.Text = "Active";
        }

        private void btnSquirtle_Click(object sender, EventArgs e)
        {
            
            string imagePath = "\"E:\\Pokemon\\384.png\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Rayquaza";
            maskedTextBox2.Text = "\"Dragon/Flying\" ";
            maskedTextBox3.Text = "Active";
        }

        private void btnJigglypuff_Click(object sender, EventArgs e)
        {
            
            string imagePath = "\"E:\\Pokemon\\382.png\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Kyogre";
            maskedTextBox2.Text = "\Water\" ";
            maskedTextBox3.Text = "Active";
        }

        private void btnMeowth_Click(object sender, EventArgs e)
        {
            
            string imagePath = "\"E:\\Pokemon\\380.png\""; 
            try
            {
                pictureBox1.Image = Image.FromFile(imagePath);
            }
            catch (Exception ex)
            {
                MessageBox.Show("‰¡Ëæ∫‰ø≈Ï√Ÿª¿“æ: " + ex.Message);
            }
            maskedTextBox1.Text = "Latias";
            maskedTextBox2.Text = "Dragon/Psychic";
            maskedTextBox3.Text = "Active";
        }

        private void label1_Click(object sender, EventArgs e)
        {
            pictureBox1.SizeMode = PictureBoxSizeMode.StretchImage;
            pictureBox1.Image = null;
            lblPokemonName.Text = "Name: ";
            lblPokemonType.Text = "Type: ";
            lblPokemonStatus.Text = "Status: ";
        }


        private void label2_Click(object sender, EventArgs e)
        {

        }

        private void label3_Click(object sender, EventArgs e)
        {

        }

        private void label4_Click(object sender, EventArgs e)
        {

        }

    }
}
        }
    }
}
