# Flutter
To run Flutter app in kiosk mode, we have to disable the GTK header bar (toolbar containing the window title, minimize and close buttons).

This is done in `linux/my_application.cc`. Simply remove/comment out the following lines:
```
GtkHeaderBar *header_bar = GTK_HEADER_BAR(gtk_header_bar_new());
gtk_widget_show(GTK_WIDGET(header_bar));
gtk_header_bar_set_title(header_bar, "gallery");
gtk_header_bar_set_show_close_button(header_bar, TRUE);
gtk_window_set_titlebar(window, GTK_WIDGET(header_bar));
```

Build same as always:
```
flutter build linux
```