# MYKxMenu

swift version of KxMenu

here is the photo

 ![image](https://github.com/marshallYin/MYKxMenu/raw/master/photo.png)
 
 Usage（用法）
 
 let menuArray = [
 
  KxMenuItem(title: "雷达", image: UIImage(named: "popover_icon_radar"), target: self, action: "leftButtonDidTouch"),
  
  KxMenuItem(title: "扫一扫", image: UIImage(named: "popover_icon_qrcode"), target: self, action: "leftButtonDidTouch")
  
  ]



Configuration(设置)

let options = OptionalConfiguration(

font: UIFont.boldSystemFontOfSize(16), 

arrowSize: 9, marginXSpacing: 7, 

marginYSpacing: 9,    // MenuItem左右边距

intervalSpacing: 25,  // MenuItem上下边距

menuCornerRadius: 6.5,  

maskToBackground: false,   

shadowOfMenu: false,   // 是否添加菜单阴影

hasSeperatorLine: true,   // 是否设置分割线

seperatorLineHasInsets: false, 

textColor: Color(R: 1,G: 1, B: 1), 

menuBackgroundColor: Color(R: 96/255,G: 96/255, B: 96/255)   // 菜单底色

)  

Show the Menu  （显示菜单）

KxMenu.showMenuInView(UIApplication.sharedApplication().keyWindow!, fromRect: CGRect(origin: CGPoint(x: 

sender.frame.origin.x , y: sender.frame.origin.y + 20), size: CGSize(width: sender.frame.size.width + 20, height: 

sender.frame.size.height)), menuItems: menuArray, withOptions: options)
