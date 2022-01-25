### 消息的设计
包括：
- 上行消息
- 下行消息
-  任务消息
-  扩展消息

**下行消息:**
``` proto
message DownMessage {
    int32 ReplyIndex = 1;
    float MaxVelocity = 2;
    repeated int32 ControlRegionIds = 3[packed = true];

    int64 ReportTaskId = 4;
    int32 ReportTaskStatus = 5;
    repeated int32 ReportTaskStatusDetail = 6[packed = true];
}

```

对应的CS类文件:
``` c#
public class DownMessage
{
    public int ReplyIndex { get; set; }
    public float MaxVelocity { get; set; }
    public List<int> ControlRegionIds { get; set; }

    public long ReportTaskId { get; set; }
    public int ReportTaskStatus { get; set; }
    public List<int> ReportTaskStatusDetail { get; set; }
}
```

对应的Cs接口文件:
``` c#
public interface IDownMessage
{
    int ReplyIndex { get; set; }
    float MaxVelocity { get; set; }
    List<int> ControlRegionIds { get; set; }

    long ReportTaskId { get; set; }
    int ReportTaskStatus { get; set; }
    List<int> ReportTaskStatusDetail { get; set; }
}
```

上行消息:
``` proto
message UpMessage {
    int32 ReplyIndex = 1;
    float MaxVelocity = 2;
    repeated int32 ControlRegionIds = 3[packed = true];

    int64 ReportTaskId = 4;
    int32 ReportTaskStatus = 5;
    repeated int32 ReportTaskStatusDetail = 6[packed = true];
}
```

### 任务消息
``` proto
message TaskMessage {
    int64 TaskId = 1;
    int32 TaskStatus = 2;
    int32 TaskOperationType = 3;
    repeated int32 PathNo = 4[packed = true];
    TaskIncidental Incidental = 5;
}

message TaskIncidental {
    int32 IncidentalType = 1;
    int32 IncidentalValue = 2;
}
```

