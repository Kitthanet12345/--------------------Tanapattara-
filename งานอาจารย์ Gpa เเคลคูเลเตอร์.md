namespace WinFormsApp5
{
    public partial class Form1 : Form
    {
        private List<double> gpaxList = new List<double>(); // สร้าง List ที่จะเก็บค่า GPAX ที่ป้อนเข้ามา
        private GPACalculator calculator = new GPACalculator();// สร้างตัวแปรสำหรับคำนวณค่า GPAX
    
    {
        public Form1()
        {
            InitializeComponent(); // ทำการกำหนดค่าต่างๆ ของ UI


        }
     


        private void button1_Click(object sender, EventArgs e)
        {
            try
            {
                double gpax = double.Parse(tbGPAx.Text); // รับค่าจาก TextBox tbGPAx และแปลงเป็น double
                gpaxList.Add(gpax);  // เก็บค่าที่ป้อนเข้ามาใน gpaxList
                calculator.AddGPAX(gpax);// ส่งค่าที่ป้อนมาให้ calculator เพื่อเก็บไว้ใน calculator

                UpdateDisplay();// อัพเดท UI เพื่อแสดงค่าต่างๆ
                tbGPAx.Clear(); // เคลียร์ TextBox หลังจากป้อนค่า
            }
            catch (FormatException)
            {
                MessageBox.Show("please enter a valid GPAX ", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error); // แจ้งเตือนกรณีป้อนค่าผิด
            }
            catch (OverflowException)
            {
                MessageBox.Show("GPAX must be between 0 and 4.", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);// แจ้งเตือนหากค่า GPAX เกินช่วง 0-4
            }
        }
        }


        private void UpdateDisplay()
        {
            tbGPAx.Text = calculator.CalculateAverageGPAX().ToString("0.00");  // แสดงค่าเฉลี่ย GPAX
            tbCount.Text = calculator.GetCount().ToString(); // แสดงจำนวน GPAX
            tbMax.Text = calculator.GetMaxGPAX().ToString("0.00");// แสดงค่า GPAX สูงสุด
            tbMin.Text = calculator.GetMinGPAX().ToString("0.00"); // แสดงค่า GPAX ต่ำสุด
        }

        using System;
        using System.Collections.Generic;
        using System.Linq;
        using System.Text;
        using System.Threading.Tasks;

namespace WinFormsApp1
    {
        internal class GPACalculator
        {
            private List<double> gpaxList = new List<double>(); สร้าง List เพื่อเก็บค่า GPAX

            public void AddGPAX(double gpax)
            {
                gpaxList.Add(gpax); // เพิ่มค่า GPAX ที่รับเข้ามาไปเก็บใน List
            }

            public double CalculateAverageGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0; // ถ้าผู้ใช้ยังไม่ได้ป้อนค่าเลย ให้คืนค่าเป็น 0
                }
                return gpaxList.Average();  // คำนวณค่าเฉลี่ยของ GPAX
            }

            public int GetCount()
            {
                return gpaxList.Count; // คืนค่าจำนวน GPAX ที่ผู้ใช้ป้อนมา
            }

            public double GetMaxGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0;  // ถ้าผู้ใช้ยังไม่ได้ป้อนค่าเลย ให้คืนค่าเป็น 0
                }
                return gpaxList.Max(); // คืนค่ามากที่สุดใน gpaxList
            }

            public double GetMinGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0; // ถ้าผู้ใช้ยังไม่ได้ป้อนค่าเลย ให้คืนค่าเป็น 0
                }
                return gpaxList.Min();  // คืนค่าต่ำที่สุดใน gpaxList

            }
    }
}
