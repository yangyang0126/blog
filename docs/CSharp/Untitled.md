# 图形基础

## Pen

![](http://cdn.zhaojingyi0126.com/image-20200427140614076.png)

```c#
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace ExamplePen
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        protected override void OnPaint(PaintEventArgs e)
        {
            Graphics g = e.Graphics;
            using (Pen bluePen = new Pen(Color.Blue, 1))
            {
                if (ClientRectangle.Height / 10 > 0)
                {
                    for (int y = 0; y < ClientRectangle.Height; y += ClientRectangle.Height / 10)
                    {
                        g.DrawLine(bluePen, new Point(0, 0), new Point(ClientRectangle.Width, y));
                    }
                }
            }
        }
    }
}
```

### Brush

添加`using System.Drawing.Drawing2D;`