# EBS

## Snapshot
https://docs.aws.amazon.com/ko_kr/AWSEC2/latest/UserGuide/EBSSnapshots.html

특정 시점 스냅샷을 만들어 S3에 Amazon EBS 볼륨의 증분식 데이터 백업 (incremental backups of EBS volumes)

## Apply Encryption While Copying a Snapshot
1) Create a snapshot of your unencrypted EBS volume. This snapshot is also unencrypred
2) Copy the snapshot while applying encryption parameters. The resulting target snapshot is encrypted.
3) Restore the encrypted snapshot to a new volume, which is also encrypted.
