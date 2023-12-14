# How-to-show-badges-in-.NET-MAUI-Avatar-View
This section is explains how to show badge in .NET MAUI AvatarView

#   Getting Started With .NET MAUI Avatar View (SfAvatarView)

## Adding .NET MAUI Avatar View reference
The Syncfusion .NET MAUI controls are available in Nuget.org. To add .NET MAUI Avatar View to your project, open the NuGet package manager in Visual Studio, search for Syncfusion.Maui.Core and then install it.

## Adding a namespace
Add the following namespace to add .NET MAUI Avatar View

**[XAML]**

```
xmlns:sfavatar="clr-namespace:Syncfusion.Maui.Core;assembly=Syncfusion.Maui.Core"
```
##  Adding the .NET MAUI Avatar View control
You can add a custom image for displaying in .NET MAUI Avatar View using the ImageSource property.

**[XAML]**

```
<ContentPage.Content>
<Grid>
    <sfavatar:SfAvatarView ContentType="Custom"
                           ImageSource="alex.png"
                           VerticalOptions="Center"
                           HorizontalOptions="Center"   
                           HeightRequest="50"
                           CornerRadius="25"
                           WidthRequest="50" />
</Grid>
</ContentPage.Content>
```

**[C#]**

```
using Syncfusion.Maui.Core;

namespace AvatarViewGettingStarted
{
    public partial class MainPage : ContentPage
    {
        public MainPage()
        {
            InitializeComponent();
            
	        //main grid
            Grid mainGrid = new Grid();

            // Create an SfAvatarView control.
            SfAvatarView avatarview = new SfAvatarView();
            avatarview.VerticalOptions = LayoutOptions.Center;
            avatarview.HorizontalOptions = LayoutOptions.Center;
            avatarview.BackgroundColor = Color.FromRgba("#ffb6c1");
            avatarview.ContentType = ContentType.Custom;
            avatarview.ImageSource = "alex.png";
            avatarview.WidthRequest = 50;
            avatarview.HeightRequest = 50;
            avatarview.CornerRadius = 25;
            mainGrid.Children.Add(avatarview);
            this.Content = mainGrid;
        }
    }
}

```

## How to show badges in .NET MAUI AvatarView

**[XAML]**
```
 <Grid>
            <core:SfBadgeView
                BadgeText=""
                HeightRequest="65"
                HorizontalOptions="Center"
                VerticalOptions="Center"
                WidthRequest="65">
                <core:SfBadgeView.Content>
                    <Grid>
                        <core:SfAvatarView
                            AvatarName="Alex"
                            ContentType="Initials"
                            CornerRadius="25"
                            HeightRequest="50"
                            HorizontalOptions="Center"
                            VerticalOptions="Center"
                            WidthRequest="50" />
                    </Grid>
                </core:SfBadgeView.Content>
                <core:SfBadgeView.BadgeSettings>
                    <core:BadgeSettings
                        Position="BottomRight"     
                        FontFamily="SegmentIcon"
                        Offset="-5,-5" />
                </core:SfBadgeView.BadgeSettings>
            </core:SfBadgeView>
        </Grid>
 ```
 ## How to run this application?

To run this application, you need to first clone the How-to-show-badges-in-.NET-MAUI-Avatar-View repository and then open it in Visual Studio 2022. Now, simply build and run your project to view the output.

## <a name="troubleshooting"></a>Troubleshooting ##
### Path too long exception
If you are facing path too long exception when building this example project, close Visual Studio and rename the repository to short and build the project.

## License

Syncfusion has no liability for any damage or consequence that may arise by using or viewing the samples. The samples are for demonstrative purposes, and if you choose to use or access the samples, you agree to not hold Syncfusion liable, in any form, for any damage that is related to use, for accessing, or viewing the samples. By accessing, viewing, or seeing the samples, you acknowledge and agree Syncfusion’s samples will not allow you seek injunctive relief in any form for any claim related to the sample. If you do not agree to this, do not view, access, utilize, or otherwise do anything with Syncfusion’s samples.