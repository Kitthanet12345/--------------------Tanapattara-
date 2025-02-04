namespace WinFormsApp5
{
    public partial class Form1 : Form
    {
        private List<double> gpaxList = new List<double>(); // ���ҧ List �����纤�� GPAX ����͹�����
        private GPACalculator calculator = new GPACalculator();// ���ҧ���������Ѻ�ӹǳ��� GPAX
    
    {
        public Form1()
        {
            InitializeComponent(); // �ӡ�á�˹���ҵ�ҧ� �ͧ UI


        }
     


        private void button1_Click(object sender, EventArgs e)
        {
            try
            {
                double gpax = double.Parse(tbGPAx.Text); // �Ѻ��Ҩҡ TextBox tbGPAx ����ŧ�� double
                gpaxList.Add(gpax);  // �纤�ҷ���͹������ gpaxList
                calculator.AddGPAX(gpax);// �觤�ҷ���͹����� calculator ���������� calculator

                UpdateDisplay();// �Ѿഷ UI �����ʴ���ҵ�ҧ�
                tbGPAx.Clear(); // ������ TextBox ��ѧ�ҡ��͹���
            }
            catch (FormatException)
            {
                MessageBox.Show("please enter a valid GPAX ", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error); // ����͹�óջ�͹��ҼԴ
            }
            catch (OverflowException)
            {
                MessageBox.Show("GPAX must be between 0 and 4.", "Error", MessageBoxButtons.OK, MessageBoxIcon.Error);// ����͹�ҡ��� GPAX �Թ��ǧ 0-4
            }
        }
        }


        private void UpdateDisplay()
        {
            tbGPAx.Text = calculator.CalculateAverageGPAX().ToString("0.00");  // �ʴ��������� GPAX
            tbCount.Text = calculator.GetCount().ToString(); // �ʴ��ӹǹ GPAX
            tbMax.Text = calculator.GetMaxGPAX().ToString("0.00");// �ʴ���� GPAX �٧�ش
            tbMin.Text = calculator.GetMinGPAX().ToString("0.00"); // �ʴ���� GPAX ����ش
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
            private List<double> gpaxList = new List<double>(); ���ҧ List �����纤�� GPAX

            public void AddGPAX(double gpax)
            {
                gpaxList.Add(gpax); // ������� GPAX ����Ѻ��������� List
            }

            public double CalculateAverageGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0; // ��Ҽ�����ѧ������͹������ ���׹����� 0
                }
                return gpaxList.Average();  // �ӹǳ�������¢ͧ GPAX
            }

            public int GetCount()
            {
                return gpaxList.Count; // �׹��Ҩӹǹ GPAX ��������͹��
            }

            public double GetMaxGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0;  // ��Ҽ�����ѧ������͹������ ���׹����� 0
                }
                return gpaxList.Max(); // �׹����ҡ����ش� gpaxList
            }

            public double GetMinGPAX()
            {
                if (gpaxList.Count == 0)
                {
                    return 0; // ��Ҽ�����ѧ������͹������ ���׹����� 0
                }
                return gpaxList.Min();  // �׹��ҵ�ӷ���ش� gpaxList

            }
    }
}
