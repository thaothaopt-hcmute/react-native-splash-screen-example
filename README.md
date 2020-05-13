## Install
npm react-native-splash-screen

Sau đó làm theo hướng dẫn của Docs
https://github.com/crazycodeboy/react-native-splash-screen

tạo folder, tạo file cần thiết

## Chú ý với iOS
1. Tạo LaunchScreen trong Images.xcassets, sau đó drag hình vào 1x 2x 3x
2. Tạo .storyboard
    Sau khi tạo, xoá label "splashscreen", thêm ImageView
    Kéo ImageView phủ nguyên cái điện thoại luôn
    Sau đó tab chỉnh style - source các thứ bên phải
      - Image View : chọn LaunchScreen (cái này vừa tạo trên Images.xcassets) - có thể hiểu khúc này là bỏ source vào
      - View : chỗ content mode chọn mode tương ứng, thường là "Scale to fill" cho nó fullfill cả screen luôn


## Chú ý style code
Nếu dùng class func thì

    const timeOut = setTimeout(() => {
        SplashScreen.hide();
        }, 1500);
        return () => {
        clearTimeout(timeOut);
        };

trong componentDidMount

SplashScreen.hide(); - func này trong screen tiếp theo của SplashScreen, ví dụ Guide Screen, Login Screen,....