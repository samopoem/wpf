using System;
using System.Collections.Generic;
using System.IO;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Data;
using System.Windows.Documents;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Imaging;
using System.Windows.Navigation;
using System.Windows.Shapes;

namespace WpfTreeview
{
    /// <summary>
    /// Interaction logic for MainWindow.xaml
    /// </summary>
    public partial class MainWindow : Window
    {
        /// <summary>
        /// Interaction logic for MainWindow.xml
        /// </summary>
        
        #region Constructor
        public MainWindow()
        {
            /// <summary>
            /// Default constructor
            /// </summary>

            InitializeComponent();
        }
        #endregion


        #region On Loaded

        /// <summary>
        ///  When the application first opens 
        /// </summary>
        /// <param name="sender"></param>
        /// <param name="e"></param>
        private void Window_Loaded(object sender, RoutedEventArgs e)
        {
            // Get every logical drive on the machine
            foreach (var drive in Directory.GetLogicalDrives())
            {
                // Create a new item for it
                var item = new TreeViewItem();

                // Set the header and path
                item.Header = drive;
                item.Tag = drive;

                // Add a dummy item
                item.Items.Add(null);

                // Add it to main tree-view
                FolderView.Items.Add(item);
            }
        }

        #endregion
    }
}
