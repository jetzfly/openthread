#
#    Copyright (c) 2016, Nest Labs, Inc.
#    All rights reserved.
#
#    Redistribution and use in source and binary forms, with or without
#    modification, are permitted provided that the following conditions are met:
#    1. Redistributions of source code must retain the above copyright
#       notice, this list of conditions and the following disclaimer.
#    2. Redistributions in binary form must reproduce the above copyright
#       notice, this list of conditions and the following disclaimer in the
#       documentation and/or other materials provided with the distribution.
#    3. Neither the name of the copyright holder nor the
#       names of its contributors may be used to endorse or promote products
#       derived from this software without specific prior written permission.
#
#    THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
#    ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
#    WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
#    DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY
#    DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
#    (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
#    LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
#    ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
#    (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
#    SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.
#

include $(abs_top_nlbuild_autotools_dir)/automake/pre.am

# Always package (e.g. for 'make dist') these subdirectories.

DIST_SUBDIRS                                                       = \
    thread-cert                                                      \
    $(NULL)

# Always build (e.g. for 'make all') these subdirectories.

SUBDIRS                                                            = \
    $(NULL)

all:

if OPENTHREAD_BUILD_TESTS

# First, list all essential program and script tests that MUST be run.

check_PROGRAMS =

check_SCRIPTS                                                      = \
    thread-cert/Cert_5_1_01_RouterAttach.py                          \
    thread-cert/Cert_5_1_02_ChildAddressTimeout.py                   \
    thread-cert/Cert_5_1_03_RouterAddressReallocation.py             \
    thread-cert/Cert_5_1_06_RemoveRouterId.py                        \
    thread-cert/Cert_5_1_08_RouterAttachConnectivity.py              \
    thread-cert/Cert_5_1_09_REEDAttachConnectivity.py                \
    thread-cert/Cert_5_1_10_RouterAttachLinkQuality.py               \
    thread-cert/Cert_5_1_11_REEDAttachLinkQuality.py                 \
    thread-cert/Cert_5_1_12_NewRouterNeighborSync.py                 \
    thread-cert/Cert_5_1_13_RouterReset.py                           \
    thread-cert/Cert_5_2_01_BecomeActiveRouter.py                    \
    thread-cert/Cert_5_2_05_AddressQuery.py                          \
    thread-cert/Cert_5_2_07_REEDSynchronization.py                   \
    thread-cert/Cert_5_3_01_LinkLocal.py                             \
    thread-cert/Cert_5_3_07_DuplicateAddress.py                      \
    thread-cert/Cert_5_3_08_ChildAddressSet.py                       \
    thread-cert/Cert_5_5_01_LeaderReset.py                           \
    thread-cert/Cert_5_6_01_NetworkDataRegisterBeforeAttachLeader.py \
    thread-cert/Cert_5_6_02_NetworkDataRegisterBeforeAttachRouter.py \
    thread-cert/Cert_5_6_03_NetworkDataRegisterAfterAttachLeader.py  \
    thread-cert/Cert_5_6_04_NetworkDataRegisterAfterAttachRouter.py  \
    thread-cert/Cert_5_6_05_NetworkDataRegisterAfterAttachRouter.py  \
    thread-cert/Cert_5_6_06_NetworkDataExpiration.py                 \
    thread-cert/Cert_5_6_07_NetworkDataRequestREED.py                \
    thread-cert/Cert_5_6_08_ContextManagement.py                     \
    thread-cert/Cert_5_6_09_NetworkDataForwarding.py                 \
    thread-cert/Cert_5_8_01_KeySynchronization.py                    \
    thread-cert/Cert_5_8_02_KeyIncrement.py                          \
    thread-cert/Cert_5_8_03_KeyIncrementRollOver.py                  \
    thread-cert/Cert_6_1_01_RouterAttach.py                          \
    thread-cert/Cert_6_1_02_REEDAttach.py                            \
    thread-cert/Cert_6_1_03_RouterAttachConnectivity.py              \
    thread-cert/Cert_6_1_04_REEDAttachConnectivity.py                \
    thread-cert/Cert_6_1_05_RouterAttachLinkQuality.py               \
    thread-cert/Cert_6_1_06_REEDAttachLinkQuality.py                 \
    thread-cert/Cert_6_1_07_EDSynchronization.py                     \
    thread-cert/Cert_6_3_01_OrphanReattach.py                        \
    thread-cert/Cert_6_3_02_NetworkDataUpdate.py                     \
    thread-cert/Cert_6_4_01_LinkLocal.py                             \
    thread-cert/Cert_6_4_02_RealmLocal.py                            \
    thread-cert/Cert_6_5_01_ChildResetSynchronize.py                 \
    thread-cert/Cert_6_5_02_ChildResetReattach.py                    \
    thread-cert/Cert_6_6_01_KeyIncrement.py                          \
    thread-cert/Cert_6_6_02_KeyIncrementRollOver.py                  \
    thread-cert/Cert_7_1_01_BorderRouterAsLeader.py                  \
    thread-cert/Cert_7_1_02_BorderRouterAsRouter.py                  \
    thread-cert/Cert_7_1_03_BorderRouterAsLeader.py                  \
    thread-cert/Cert_7_1_04_BorderRouterAsRouter.py                  \
    thread-cert/Cert_7_1_05_BorderRouterAsRouter.py                  \
    $(NULL)

# List all other non-essential program and script tests that MAY be run.

if !OPENTHREAD_WITH_MINIMUM_SET_OF_TESTS

check_SCRIPTS                                                     += \
    thread-cert/Cert_5_1_04_RouterAddressReallocation.py             \
    thread-cert/Cert_5_1_05_RouterAddressTimeout.py                  \
    thread-cert/Cert_5_1_07_MaxChildCount.py                         \
    thread-cert/Cert_5_2_02_LeaderReject1Hop.py                      \
    thread-cert/Cert_5_2_03_LeaderReject2Hops.py                     \
    thread-cert/Cert_5_2_04_REEDUpgrade.py                           \
    thread-cert/Cert_5_3_02_RealmLocal.py                            \
    thread-cert/Cert_5_3_03_AddressQuery.py                          \
    thread-cert/Cert_5_3_04_AddressMapCache.py                       \
    thread-cert/Cert_5_3_05_RoutingLinkQuality.py                    \
    thread-cert/Cert_5_3_06_RouterIdMask.py                          \
    thread-cert/Cert_5_3_10_AddressQuery.py                          \
    thread-cert/Cert_5_5_02_LeaderReboot.py                          \
    thread-cert/Cert_5_5_03_SplitMergeChildren.py                    \
    thread-cert/Cert_5_5_04_SplitMergeRouters.py                     \
    thread-cert/Cert_5_5_05_SplitMergeREED.py                        \
    thread-cert/Cert_5_5_06_SplitWeight.py                           \
    thread-cert/Cert_5_5_07_SplitMergeThreeWay.py                    \
    thread-cert/Cert_5_5_08_SplitRoutersLostLeader.py                \
    thread-cert/Cert_6_2_01_NewPartition.py                          \
    thread-cert/Cert_6_2_02_NewPartition.py                          \
    $(NULL)

endif # OPENTHREAD_WITH_ESSENTIAL_TESTS_ONLY

TESTS_ENVIRONMENT                                                  = \
    export                                                           \
    top_srcdir='$(top_srcdir)'                                       \
    VERBOSE=1;                                                       \
    $(NULL)

TESTS                                                              = \
    $(check_PROGRAMS)                                                \
    $(check_SCRIPTS)                                                 \
    $(NULL)

endif # OPENTHREAD_BUILD_TESTS

include $(abs_top_nlbuild_autotools_dir)/automake/post.am
