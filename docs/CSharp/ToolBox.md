# 控件

## 按钮类

Button+TextBox

![](http://cdn.zhaojingyi0126.com/IMG/image-20200415123207606.png)

```c#
namespace WindowsFormsApplication1
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private int nCounter;
        private void ShowCounter()
        {
            string strMsg = this.nCounter.ToString("D2");
            this.TextResult.Text = strMsg;
        }

        private void Form1_Load(object sender, EventArgs e)
        {
            this.nCounter = 50;
            this.ShowCounter();
        }

        private void btnInc_Click(object sender, EventArgs e)
        {
            this.nCounter++;
            this.ShowCounter();
        }

        private void btnDes_Click(object sender, EventArgs e)
        {
            this.nCounter--;
            this.ShowCounter();
        }

        private void btnMsg_Click(object sender, EventArgs e)
        {
            string strMsg = "当前计数器=" + this.nCounter.ToString("D2");  
            //D2显示2位数字，D3显示3位数，前面补0
            MessageBox.Show(strMsg, "提示");
        }
    }
}

```



## 文本类控件

### TextBox

Label+TextBox

![](http://cdn.zhaojingyi0126.com/IMG/image-20200415130815576.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    textBox1.PasswordChar = '@';
    textBox2.UseSystemPasswordChar = true;
}
```



### RichTextBox

富文本框控件 

(1) Redo方法：用来重做上次被撤销的操作。

(2) Find方法：用来从RichTextBox控件中查找指定的字符串。

(3) LoadFile方法：使用LoadFile方法可以将文本文件、RTF文件装入RichTextBox控件。

![](http://cdn.zhaojingyi0126.com/IMG/image-20200415140552978.png)



```c#
private void Form1_Load(object sender, EventArgs e)
{
    richTextBox1.LoadFile("D:\\Coding\\blog\\CSharp\\test.rtf", RichTextBoxStreamType.RichText);
}
```

## 选择性控件

### RadioButton

### CheckBox

![](http://cdn.zhaojingyi0126.com/IMG/image-20200415153224139.png)

```c#
public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {
        }

        private String strGender = "";  // 性别
        private String strHobby = "";  // 爱好

        //单击按钮
        private void button_Click(object sender, EventArgs e)
        {
            labelReturn.Text = "姓名" + textName.Text + "，性别" + strGender + "，爱好是" + strHobby;
        }

        private void radioMan_CheckedChanged(object sender, EventArgs e)
        {
            strGender = "男";
        }

        private void radioWoman_CheckedChanged(object sender, EventArgs e)
        {
            strGender = "女";
        }

        private void checkWeb_CheckedChanged(object sender, EventArgs e)
        {
            if(checkWeb.Checked)
            {
                strHobby = strHobby + checkWeb.Text;
            }
            else
            {
                strHobby.Replace(checkWeb.Text + "</br>", "");
                strHobby.Trim();
            }
        }

        private void checkRead_CheckedChanged(object sender, EventArgs e)
        {
            if (checkRead.Checked)
            {
                strHobby = strHobby + checkRead.Text;
            }
            else
            {
                strHobby.Replace(checkRead.Text + "</br>", "");
                strHobby.Trim();
            }
        }

        private void checkClimb_CheckedChanged(object sender, EventArgs e)
        {
            if (checkClimb.Checked)
            {
                strHobby = strHobby + checkClimb.Text;
            }
            else
            {
                strHobby.Replace(checkClimb.Text + "</br>", "");
                strHobby.Trim();
            }
        }
    }
```

## 容器类控件

### Panel

![](http://cdn.zhaojingyi0126.com/IMG/image-20200415160445611.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    panel1.BorderStyle = BorderStyle.FixedSingle;  // 边框样式
    panel1.AutoScroll = true;  // 显示滚动条
}
```

### TabControl

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416090755667.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    tabControl1.Appearance = TabAppearance.Normal;
}

private void button1_Click(object sender, EventArgs e)
{    
    string Title = "新增选项卡" + (tabControl1.TabCount + 1).ToString();
    TabPage MyTabPage = new TabPage(Title);
    tabControl1.TabPages.Add(MyTabPage);
    MessageBox.Show("现有" + tabControl1.TabCount + "个选项卡");
}

private void button2_Click(object sender, EventArgs e)
{
    if (tabControl1.SelectedIndex == 0)
    {
        MessageBox.Show("请选择要移除的选项卡");
    }
    else
    {
        tabControl1.TabPages.Remove(tabControl1.SelectedTab);
    }      
}
```

## 其他控件

### ComboBox

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416100026582.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    comboBox1.Items.Clear();
    comboBox1.Items.Add("中国");
    comboBox1.Items.Add("美国");
    comboBox1.Items.Add("日本");
    comboBox1.Items.Add("英国");
    comboBox1.Items.Add("加拿大");
    comboBox1.Items.Add("澳大利亚");
    this.comboBox1.AutoCompleteMode = AutoCompleteMode.SuggestAppend;
    this.comboBox1.AutoCompleteSource = AutoCompleteSource.ListItems;
}
```

### PictureBox

### ProgressBar

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416100752703.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    this.progressBar1.Maximum = 1000;
    this.progressBar1.Minimum = 0;
    this.progressBar1.Step = 2;
    for (int i = 0; i <= 1000; i++)
    {
        if (i % 2== 0)
        {
            progressBar1.PerformStep();
        }
    }
}
```

### DataTimePicker

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416102257294.png)

## 菜单

### MenuStrip 

菜单栏

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416104919786.png)

## 工具栏和状态栏

### ToolStrip 

工具栏

### StatusStrip 

状态栏

## 对话框

### OpenFileDialog+SaveFileDialog

打开、保存对话框

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416124946689.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    button1.Enabled = true;
    button2.Enabled = false;
}

private void button1_Click(object sender, EventArgs e)
{
    openFileDialog1.FileName = "";
    openFileDialog1.Filter = "RTF File(*.trf)|*.RTF|TXT File(*.txt)|*.txt";
    openFileDialog1.ShowDialog();
    if (openFileDialog1.FileName != "")
    {
        switch (openFileDialog1.FilterIndex)
        {
            case 1:
                richTextBox1.LoadFile(openFileDialog1.FileName, RichTextBoxStreamType.RichText);
                break;
            case 2:
                richTextBox1.LoadFile(openFileDialog1.FileName, RichTextBoxStreamType.PlainText);
                break;
        }
        button2.Enabled = true;
    }
}

private void button2_Click(object sender, EventArgs e)
{
    saveFileDialog1.Filter = "RTF File(*.trf)|*.RTF|TXT File(*.txt)|*.txt";
    if (saveFileDialog1.ShowDialog() == DialogResult.OK)
    {
        switch (openFileDialog1.FilterIndex)
        {
            case 1:
                richTextBox1.SaveFile(saveFileDialog1.FileName, RichTextBoxStreamType.RichText);
                break;
            case 2:
                richTextBox1.SaveFile(saveFileDialog1.FileName, RichTextBoxStreamType.PlainText);
                break;
        }
    }
}
```

### FolderBrowserDialog 

打开文件夹



### FrontDialog



字体对话框



### ColorDialog

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416144228756.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    richTextBox1.Text = "这是一段示例文字\n这是一段示例文字\n这是一段示例文字\n这是一段示例文字";
}

private void button1_Click(object sender, EventArgs e)
{
    fontDialog1.AllowVectorFonts = true;    // 允许选择矢量字体
    fontDialog1.AllowVerticalFonts = true;    // 水平字体和垂直字体
    fontDialog1.FixedPitchOnly = false;    // 不固定字体间距
    fontDialog1.MaxSize = 72;
    fontDialog1.MinSize = 5;
    if (fontDialog1.ShowDialog() == DialogResult.OK)
    {
        if (richTextBox1.SelectedText == "")
        {
            richTextBox1.SelectAll();
            richTextBox1.SelectionFont = fontDialog1.Font;
        }
        else
        {
            richTextBox1.SelectionFont = fontDialog1.Font;
        }
    }
}

private void button2_Click(object sender, EventArgs e)
{
    colorDialog1.AllowFullOpen = true;
    colorDialog1.AnyColor = true;
    colorDialog1.SolidColorOnly = false;
    if (colorDialog1.ShowDialog() == DialogResult.OK)
    {
        if (richTextBox1.SelectedText == "")
        {
            richTextBox1.SelectAll();
            richTextBox1.SelectionColor = colorDialog1.Color;
        }
        else
        {
            richTextBox1.SelectionColor = colorDialog1.Color;
        }
    }
}
```

## 列表

### ListBox

![](http://cdn.zhaojingyi0126.com/IMG/image-20200416094511209.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
}

private void button1_Click(object sender, EventArgs e)
{
    if (this.textBox1.Text != "")
    {
        this.listBox1.Items.Add(this.textBox1.Text);
        this.textBox1.Text = "";
    }
}

private void button2_Click(object sender, EventArgs e)
{
    int nSelectedIndex = listBox1.SelectedIndex;
    if (nSelectedIndex < listBox1.Items.Count && nSelectedIndex > -1)
    {
        this.listBox1.Items[nSelectedIndex] = this.textBox1.Text;
    }
}
```

### ListView

![](http://cdn.zhaojingyi0126.com/image-20200417100032037.png)

```c#
private void Form1_Load(object sender, EventArgs e)
{
    InitListView(this.listView1);
    InitOtherControl();

}
private void InitOtherControl()
{
    // DropDownList只能在下拉列表里面选，不能手动输入
    comboBox1.DropDownStyle = ComboBoxStyle.DropDownList;
    comboBox1.Items.Add("LargeIcon");
    comboBox1.Items.Add("SmallIcon");
    comboBox1.Items.Add("List");
    comboBox1.Items.Add("Title");
    comboBox1.Items.Add("Details");
    comboBox1.SelectedIndexChanged += new EventHandler(comboBox1_SelectedIndexChanged);
    checkBox1.CheckedChanged += new EventHandler(checkBox1_CheckedChanged);
}
private void InitListView(ListView listView)
{
    ColumnHeader Header1 = new ColumnHeader();
    Header1.Width = 100;
    Header1.Text = "名称";
    ColumnHeader Header2 = new ColumnHeader();
    Header2.Width = 100;
    Header2.Text = "编号";
    ColumnHeader Header3 = new ColumnHeader();
    Header3.Width = 100;
    Header3.Text = "描述";

    listView1.Columns.Add(Header1);
    listView1.Columns.Add(Header2);
    listView1.Columns.Add(Header3);

    listView1.GridLines = true;
    listView1.FullRowSelect = true;
    listView1.HoverSelection = false;
    listView1.MultiSelect = false;

    ImageList LargeImageList = new ImageList();
    LargeImageList.ImageSize = new Size(80, 80);
    LargeImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\pen.png"));
    LargeImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\book.png"));
    LargeImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\box.png"));
    listView1.LargeImageList = LargeImageList;

    ImageList SmallImageList = new ImageList();
    SmallImageList.ImageSize = new Size(30, 30);
    SmallImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\pen.png"));
    SmallImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\book.png"));
    SmallImageList.Images.Add(Image.FromFile("C:\\Users\\admin\\Pictures\\Camera Roll\\box.png"));
    listView1.SmallImageList = SmallImageList;

    ListViewItem lv1 = new ListViewItem("笔");
    lv1.SubItems.Add("001");
    lv1.SubItems.Add("这是一支钢笔");
    lv1.ImageIndex = 0;
    ListViewItem lv2 = new ListViewItem("书籍");
    lv2.SubItems.Add("002");
    lv2.SubItems.Add("这是一本书");
    lv2.ImageIndex = 1;
    ListViewItem lv3 = new ListViewItem("盒子");
    lv3.SubItems.Add("003");
    lv3.SubItems.Add("这是一个盒子");
    lv3.ImageIndex = 2;

    listView1.Items.Add(lv1);
    listView1.Items.Add(lv2);
    listView1.Items.Add(lv3);

    listView1.SelectedIndexChanged += new EventHandler(listView1_SelectedIndexChanged);

}

private void comboBox1_SelectedIndexChanged(object sender, EventArgs e)
{
    switch (comboBox1.Text)
    {
        case "LargeIcon":
            this.listView1.View = View.LargeIcon;
            break;
        case "SmallIcon":
            this.listView1.View = View.SmallIcon;
            break;
        case "List":
            this.listView1.View = View.List;
            break;
        case "Title":
            this.listView1.View = View.Tile;
            break;
        case "Details":
            this.listView1.View = View.Details;
            break;
    }
}

private void checkBox1_CheckedChanged(object sender, EventArgs e)
{
    this.listView1.CheckBoxes = this.checkBox1.Checked;

}

private void listView1_SelectedIndexChanged(object sender, EventArgs e)
{
    if (this.listView1.SelectedItems.Count > 0)
    {
        string strMessage = "名称:" + this.listView1.SelectedItems[0].SubItems[0].Text + "\r\n";
        strMessage += "编号:" + this.listView1.SelectedItems[0].SubItems[1].Text + "\r\n";
        strMessage += "描述:" + this.listView1.SelectedItems[0].SubItems[2].Text + "\n";
        this.textBox1.Text = strMessage;
    }
}
```

## 树形控件

### TreeView

![](http://cdn.zhaojingyi0126.com/image-20200427124749622.png)

```c#
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace TreeViewDemo
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void InitTreeView(TreeView treeView)
        {
            treeView.CheckBoxes = false;
            treeView.FullRowSelect = true;
            ImageList imageList = new ImageList();
            imageList.Images.Add(new Icon("D:\\C#\\Folder.ico"));
            imageList.Images.Add(new Icon("D:\\C#\\OpenFolder.ico"));
            imageList.Images.Add(new Icon("D:\\C#\\Book.ico"));
            treeView.ImageList = imageList;

            treeView.LabelEdit = false;
            treeView.PathSeparator = "\\";
            treeView.Scrollable = true;
            treeView.ShowLines = true;
            treeView.ShowNodeToolTips = true;
            treeView.ShowPlusMinus = true;
            treeView.ShowRootLines = true;

            treeView.AfterSelect += new TreeViewEventHandler(treeView1_AfterSelect);
        }
        
        private void Form1_Load(object sender, EventArgs e)
        {
            this.InitTreeView(this.treeView1);
            this.AddNode(this.treeView1);
        }

        private void button1_Click(object sender, EventArgs e)
        {
            this.treeView1.ExpandAll();
        }

        private void button2_Click(object sender, EventArgs e)
        {
            this.treeView1.CollapseAll();
        }

        public class Book
        {
            public string BookName = string.Empty;
            public string Author = string.Empty;
            public string Price = string.Empty;
        }

        private void treeView1_AfterSelect(object sender, TreeViewEventArgs e)
        {
            if (e.Node.Tag != null)
            {
                Book book = e.Node.Tag as Book;
                this.textPath.Text = e.Node.FullPath;
                this.textBookName.Text = book.BookName;
                this.textAuthor.Text = book.Author;
                this.textPrice.Text = book.Price;
            }
        }

        private void AddNode(TreeView treeView)
        {
            
            TreeNode MainNode = treeView.Nodes[0];
            treeView.BeginUpdate();
            MainNode.Nodes.Clear();

            TreeNode Catalog1 = new TreeNode("计算机技术");
            Catalog1.ImageIndex = 0;
            Catalog1.SelectedImageIndex = 1;

            Book Book1 = new Book();
            Book1.BookName = "计算机技术";
            Book1.Author = "小王";
            Book1.Price = "20.00";
            TreeNode BookNode1 = new TreeNode(Book1.BookName);
            BookNode1.ImageIndex = 2;
            BookNode1.SelectedImageIndex = 2;
            BookNode1.Tag = Book1;

            Book Book2 = new Book();
            Book2.BookName = "Windows技术";
            Book2.Author = "小李";
            Book2.Price = "60.00";
            TreeNode BookNode2 = new TreeNode(Book2.BookName);
            BookNode2.ImageIndex = 2;
            BookNode2.SelectedImageIndex = 2;
            BookNode2.Tag = Book2;

            Catalog1.Nodes.Add(BookNode1);
            Catalog1.Nodes.Add(BookNode2);
            MainNode.Nodes.Add(Catalog1);

            TreeNode Catalog2 = new TreeNode("文学小说");
            Catalog2.ImageIndex = 0;
            Catalog2.SelectedImageIndex = 1;

            Book Book3 = new Book();
            Book3.BookName = "Love";
            Book3.Author = "LN";
            Book3.Price = "39.00";
            TreeNode BookNode3 = new TreeNode(Book3.BookName);
            BookNode3.ImageIndex = 2;
            BookNode3.SelectedImageIndex = 2;
            BookNode3.Tag = Book3;

            Book Book4 = new Book();
            Book4.BookName = "Hello";
            Book4.Author = "Lily";
            Book4.Price = "21.00";
            TreeNode BookNode4 = new TreeNode(Book4.BookName);
            BookNode4.ImageIndex = 2;
            BookNode4.SelectedImageIndex = 2;
            BookNode4.Tag = Book4;

            Catalog2.Nodes.Add(BookNode3);
            Catalog2.Nodes.Add(BookNode4);
            MainNode.Nodes.Add(Catalog2);
            treeView.EndUpdate();
        }
    }
}
```

## 表格控件

### GridView

### DataList

### Repeater

### DetailsView

### FormView



