# Copyright © 2022 sealos.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.

# Build the manager binary
#dev
#FROM gcr.dockerproxy.com/distroless/static:nonroot
#production
FROM gcr.io/distroless/static:nonroot
WORKDIR /
ARG TARGETARCH
#RUN apt update && apt install apt-utils && apt install -y --no-install-recommends ca-certificates
USER 65532:65532
COPY bin/controller-infra-$TARGETARCH /manager
ENTRYPOINT ["/manager"]
