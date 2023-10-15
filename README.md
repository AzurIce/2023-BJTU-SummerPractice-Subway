# 基于TCN模型与GTFS实时数据的地铁客流信息实时预测系统

这个题目本来叫做「基于时间序列模型的地铁客流量预测系统」，但是其实不太贴切。
功能：
- 纽约地铁实时位置显示
- 纽约地铁站点实时客流量热力图显示
- 纽约地铁站点实时客流量数据图表显示
- 纽约地铁站点未来客流量预测及数据图表显示

或许应该叫「纽约地铁实时客流信息显示系统」

实时数据来源使用了 GTFS 技术，而客流预测使用了 TCN 模型

那么或许可以叫「基于TCN模型与GTFS实时数据的地铁客流信息实时预测系统」


```mermaid
gantt
    title 第三小组任务进度
    dateFormat  YYYY-MM-DD
    section 整体项目
    项目											   :2023-07-03, 12d
    立项           									 :done, a1, 2023-07-03, 1d
    中期答辩                                            :done, a2, 2023-07-10, 1d
    答辩           									 :done, a1, 2023-07-14, 1d
    section 前端
    创建项目                                          :done, create_project, 2023-07-03, 1d
    
    基本项目结构                                      :done, frontend_basic, after create_project, 1d
    登陆、注册界面                                    :done, login_page, after create_project, 1d
    
    纽约地铁线路数据获取解析                             :done, route_data, after create_project, 1d
    接入 MapBox API 完成基本地铁线路可视化（固定）         :done, map_basic, after frontend_basic, 1d
    
    接入 MTA GTFS 完成基本的地铁位置可视化（离散的）       :done, pos_basic, after map_basic, 2d
    与后端登录注册对接                                 :done, login_page_connect, 2023-07-07,  1d
    
    接入 goodservice API 实现地铁线路可视化（实时）      :done, route_realtime, 2023-07-07, 2d
    实现地铁位置可视化（实时）                          :done, pos_realtime, 2023-07-08, 3d
    
    与后端对接完成人流量热力图可视化                     :heat_map, after pos_realtime, 2d
    
    section 后端
    创建项目                                          :done, create_backend, 2023-07-03, 1d
    登录                                            :done, login, 2023-07-04, 2d
    注册                                            :done, register, 2023-07-06, 2d
    与算法端对接实现真实、预测数据获取                    :done, data, 2023-07-07, 4d
    数据查询接口添加时间范围                           :done, data_time, 2023-07-10, 1d
    section 算法
    数据集获取                                      :done, data_set, 2023-07-03, 1d
    数据集预处理                                     :done, data_set, 2023-07-04, 2d 
    特征选择及特征提取                                 	:done, data_set, 2023-07-04, 3d
    LSTM 算法实现                                    :done, lstm_impl, 2023-07-05, 1d
    LSTM 算法调参                                    :done, lstm_arg, 2023-07-06, 2d
    数据定期更新                                      :done, update_data, 2023-07-07, 1d
    TCN 模型实现                                      :done, tcn, 2023-07-08, 2d
    
```





